---
title: Faktisk vs. budsjett Power BI-innhold
description: "Dette emnet beskriver Faktisk vs. budsjett-innholdet for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5d52cce3cccb16f0645d9de1832ebeffbfaf3a09
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# Faktisk vs. budsjett Power BI-innhold
<a id="actual-vs-budget-power-bi-content" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Dette emnet beskriver **Faktisk vs. budsjett**-innholdet for Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet. 

# Oversikt
<a id="overview" class="xliff"></a>

Den **Faktisk vs. budsjett** Power BI-innholdet ble opprettet for personer som har ansvar for overvåking av faktiske resultater mot budsjetterte resultater i organisasjonen. **Faktisk vs. budsjett** Power BI-innhold gir oversikt over avvik i budsjettet. Du kan analysere budsjettet for gjeldende år etter kontokategori, budsjettkode, hovedkontoe, beskrivelser av hovedkontoe eller regnskapsperiode for å få en bedre forståelse av eventuelle avvik. 

# Tilgang til Power BI-innhold
<a id="accessing-the-power-bi-content" class="xliff"></a>
Hvis du bruker oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, vises rapporter fra **Faktisk vs. budsjett** Power BI-innholdet i arbeidsområdet **Finansbudsjetter og prognoser** og **CFO**.

# Rapporter som er inkludert i Power BI-innholdet
<a id="reports-that-are-included-in-the-power-bi-content" class="xliff"></a>
Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i **Faktisk vs. budsjett** Power BI-innholdet.

| Rapporter                      | Mål |
|-----------------------------|---------|
| Utgifter – faktiske i forhold til budsjett | <ul><li>Totale utgifter i inneværende år</li><li>Budsjetterte totale utgifter i inneværende år</li></ul> |
| Inntekt – faktisk i forhold til budsjett  | <ul><li>Totalomsetning i inneværende år</li><li>Budsjettert totalomsetning i inneværende år</li><ul> |
| Utgift                     | <ul><li>Totale utgifter i inneværende år</li><li>Mål for utgifter basert på budsjett </li><ul> |
| Omsetning                     | <ul><li>Totalomsetning i inneværende år</li><li>Mål for inntekter basert på budsjett </li><ul> |
| Nettoinntekt                  | <ul><li>Nettoinntekt i inneværende år</li><li>Mål for nettoinntekt basert på budsjett </li><ul> |

## Utvide Power BI-innholdet
<a id="extending-the-power-bi-content" class="xliff"></a>
Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Microsoft Dynamics 365, gode analyser. Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere innholdspakkene på Power BI.com-leieren for analyse. 

Du kan finne **Faktisk vs. budsjett**-innholdet for Power BI i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

# Forstå datamodellen og enheter
<a id="understanding-the-data-model-and-entities" class="xliff"></a>

| Enhet                    | Innhold |
|---------------------------|----------|
| Aktiviteter i øknomimodulen | Transaksjonsbeløp for økonomimodulen |
| Budsjettaktiviteter         | Transaksjonsbeløp for budsjettregisteret |
| Hovedkontoer             | Hovedkontoer rapporter kan filtreres etter |
| Regnskapskalendere          | Regnskapskalendere rapporter kan filtreres etter |
| Finanskontoer                   | Finanskontoer som kan brukes til å filtrere rapporten til den gjeldende finanskontoen |
| Budsjettkoder              | Budsjettkoder rapporter kan filtreres etter |
| Juridiske enheter            | Juridiske enheter som kan brukes til å filtrere rapporten til den gjeldende juridiske enheten |

