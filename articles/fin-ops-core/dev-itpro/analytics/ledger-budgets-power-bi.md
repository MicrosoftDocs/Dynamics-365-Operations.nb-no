---
title: Power BI-innholdet Faktisk vs. budsjett
description: Denne artikkelen beskriver Faktisk vs. budsjett-innholdet for Power BI. Det forklarer hvordan du får tilgang til rapportene og gir informasjon om datamodellen.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff57d052b66103ad716ad8d55afb4fcb095d2c02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847289"
---
# <a name="actual-vs-budget-power-bi-content"></a>Power BI-innholdet Faktisk vs. budsjett

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver **Faktisk vs. budsjett**-innholdet for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

Power BI-innholdet **Faktisk vs. budsjett** ble opprettet for personer som har ansvar for overvåking av faktiske resultater mot budsjetterte resultater i organisasjonen. Power BI-innholdet **Faktisk vs. budsjett** gir oversikt over avvik i budsjettet. Du kan analysere budsjettet for gjeldende år etter kontokategori, budsjettkode, hovedkontoe, beskrivelser av hovedkontoe eller regnskapsperiode for å få en bedre forståelse av eventuelle avvik.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet
Rapporter fra Power BI-innholdet **Faktisk i forhold til budsjett** vises i **Finansbudsjetter og prognoser**- og **CFO**-arbeidsområder.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet
Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i Power BI-innholdet **Faktisk vs. budsjett**.

| Rapporter                      | Mål                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Utgifter – faktiske i forhold til budsjett | <ul><li>Totale utgifter i inneværende år</li><li>Budsjetterte totale utgifter i inneværende år</li></ul>  |
| Inntekt – faktisk i forhold til budsjett  | <ul><li>Totalomsetning i inneværende år</li><li>Budsjettert totalomsetning i inneværende år</li><ul>     |
| Utgift                     | <ul><li>Totale utgifter i inneværende år</li><li>Mål for utgifter basert på budsjett</li><ul> |
| Omsetning                     | <ul><li>Totalomsetning i inneværende år</li><li>Mål for inntekter basert på budsjett</li><ul>   |
| Nettoinntekt                  | <ul><li>Nettoinntekt i inneværende år</li><li>Mål for nettoinntekt basert på budsjett</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

| Enhet                    | Innhold                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Aktiviteter i øknomimodulen | Transaksjonsbeløp for økonomimodulen                                       |
| Budsjettaktiviteter         | Transaksjonsbeløp for budsjettregisteret                                      |
| Hovedkontoer             | Hovedkontoer rapporter kan filtreres etter                                               |
| Regnskapskalendere          | Regnskapskalendere rapporter kan filtreres etter                                            |
| Finanskontoer                   | Finanskontoer som kan brukes til å filtrere rapporten til den gjeldende finanskontoen              |
| Budsjettkoder              | Budsjettkoder rapporter kan filtreres etter                                                |
| Juridiske enheter            | Juridiske enheter som kan brukes til å filtrere rapporten til den gjeldende juridiske enheten |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]