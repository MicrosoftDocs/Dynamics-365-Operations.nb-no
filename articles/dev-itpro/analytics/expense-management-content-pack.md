---
title: Reiseregning og utlegg for Power BI-innhold
description: Dette emnet beskriver hva som er inkludert i Power BI-innholdspakken for reiseregning.
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a07d9ed7e4c57c2444d1c2a017109509c153aad4
ms.sourcegitcommit: 4e104ad3fc4a160a06f0d031974d60abcbb62829
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "851193"
---
# <a name="expense-management-power-bi-content"></a>Reiseregning og utlegg for Power BI-innhold

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i Power BI-innholdet for reiseregning. 

## <a name="overview"></a>Oversikt
To Power BI-innholdspakker er tilgjengelige for bruk med reiseregninger i versjon 8.1 og senere. 
- Det finnes et personlig instrumentbord for ansatte som sender reiseregninger. 

  Instrumentbordet er tilpasset for å gi viktig informasjon til personer om usendte og sendte beløp samt historikk og innsikt i transaksjonsloggen for utgift. Det personlige instrumentbordet er en enkelt side som inneholder den viktigste informasjonen for brukeren.

- Det finnes et admin-instrumentbord som er utviklet for regnskapsassistenter og -ledere hos leverandører. Instrumentbordet er tilpasset mot sporing og rapportering for samlede utgifter for ansatte. Det inneholder viktige utgiftmål, for eksempel usendte utgifter, kjørelengde og gjennomsnittlige reiseregningsbeløp. Det bruker transaksjonsdata og gir aggregerte visninger av reiseregninger på tvers av alle firmaer. Det gir også en analyse per ansatt med mulighet for å legge til finansdimensjonsdata. Analyse av adminutgift-innholdet inneholder: 
  - En oversiktsside med viktige målinger av utgiftsbeløp og innsikt i rapporter for kladd, i arbeid og fullførte reiseregninger. 
  - En ansattstatistikkside for å se gjennom enkelte detaljer om en ansatt etter tid, kosttype og statistikkgruppe. 
  - En ansattsammenligningsside for å sammenligne flere ansatte over tid. 

Alle beløpene vises i selskapsvalutaen. Data for alle firmaer som vises, men hvis nødvendig kan du legge et firmafilter. 

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet
Du finner Power BI-innholdet Expense Admin Dashboard.pbix og Expense Personal Dashboard.pbix i biblioteket Delte aktiva i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).
Innholdet er tilgjengelig fra arbeidsområdet for reiseregninger som innebygd Power Bi-innhold. En utgiftseier får tilgang til personlige utgifter for seg selv, men bare regnskapsassistenter og -ledere hos leverandører har tilgang til admin-innhold for å vise alle brukerens utgiftsdata.

## <a name="refreshing-the-power-bi-content"></a>Oppdatere Power BI-innhold
Power BI-innhold for reiseregninger krever at TrvBiExpenseMeasurement-målet og BudgetActivityMeasure oppdateres fra enhetslageret. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
Innholdet inneholder et sett med rapportsider. Hver side består av et sett med mål som er visualisert som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over effektene i Power BI-innholdspakken.

**Analyse av personlige utgifter**

| Rapportside | Visualisering                             |
|-------------|-------------------------------------------|
| Mine utgifter | Antall kilometer                         |
|             | Pågående reiseregninger                |
|             | Nr. av usendte utgifter               |
|             | Personlige utgifter som skal betales              |
|             | Usendt beløp                        |
|             | Sendt beløp                          |
|             | Beløp som venter på refusjon             |
|             | Reiseregninger med beløp og status   |
|             | Sendte, men ikke godkjente reiseregninger  |
|             | Utgifter etter kosttype                     |
|             | Utgifter etter forhandler                      |
|             | Utgifter etter behandlede utgifter            |
|             | Utgifter etter prosjekt                       |
|             | Totalt transaksjonsbeløp over tid        |

**Analyse av adminutgift**

| Rapportside         | Visualisering                           |           
|---------------------|-----------------------------------------|
| Utgiftsoversikt    | Utgiftsutkastbeløp                   |
|                     | Antall utgiftsutkastlinjer           |
|                     | Utgiftsutkastlinjer                     |
|                     | Policybrudd for reiseregning        |
|                     | Utestående beløp                      |
|                     | Sendte, men ikke godkjente utgifter       |
|                     | Godkjente utgifter                       |
|                     | Samlet utgiftsbeløp                    |
|                     | Sammendrag av reiseregning                |
|                     | Utgifter etter kosttype                   |
|                     | Utgifter etter forhandler                    |
|                     | Utgifter etter ansatte                   |
|                     | Utgifter kontra prosjekt                     |
| Ansattsammenligning | Utgiftsbeløp                         |
|                     | Utgiftsbeløp over tid etter ansatt   |
| Ansattstatistikk | Reiseregninger etter kosttype            |
|                     | Personlige utgifter                       |
|                     | Reiseregninger etter statistikkgruppe     |
