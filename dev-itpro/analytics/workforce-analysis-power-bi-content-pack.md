---
title: Workforce Metrics-innhold for Power BI
description: "Dette emnet beskriver Dynamics 365 for Operations - Workforce Metrics-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2a3f611d29e041a5f05e3f93fd2330f4218b9dd1
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="workforce-metrics-power-bi-content"></a>Workforce Metrics-innhold for Power BI

[!include[banner](../includes/banner.md)]


Dette emnet beskriver Dynamics 365 for Operations - Workforce Metrics-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken.

<a name="accessing-the-content-pack"></a>Tilgang til innholdspakken
--------------------------

Du kan finne Workforce Metrics-innholdspakken i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og kobler den til Microsoft Dynamics 365 for Operations-data, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til Dynamics 365 for Operations-dataene dine, viser rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innholdspakken, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                                           | Innhold                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arbeidsstokken analyse firmanavn, avdeling, sted | Antall ansatte etter selskap, etter avdeling, etter sted og totalt antall ansatte                                                                                                                           |
| Analysejobb for antall ansatte, trinn, leder            | Antall ansatte etter jobb, etter trinn, etter leder og totalt antall ansatte                                                                                                                                      |
| Trendanalyse for antall ansatte                         | Antall ansatte inneværende år sammenlignet med fjoråret etter selskap og rullerende antall ansatte for de siste 12 månedene                                                                                                                        |
| Demografi for arbeidsstyrken                           | Antall ansatte etter alder, kjønn, etnisitet, veteranstatus, ekteskapelig status, antall heltidsstudenter, gjennomsnittlig fartstid, gjennomsnittsalder og forholdet mellom kvinnelige og mannlige ansatte |
| Stillingsanalyse                                | Åpne stillinger etter avdeling, ledig-til-besatt-stillinger, aktiv-til-inaktive-stillinger og stillinger etter avdeling                                                                                                   |
| Avgangsanalyse                               | Avgang inneværende år sammenlignet med fjoråret, avgang, gjennomsnittlig fartstid for personer som slutter, gjennomsnittsalderen for å slutte og ansatte som slutter etter årsak                                                                   |
| Personer etter avdeling                             | Ansatte med et personalnummer etter avdeling, stilling og start- og sluttdatoer for tildeling                                                                                                                       |
| Ansiennitetsanalyse                               | Liste over gjennomsnittlig antall år med arbeidserfaring etter selskap og ansiennitet                                                                                                                                                              |
| Jubileer og arbeidserfaring               | Ansatte etter arbeidserfaring og jubileer                                                                                                                                                                    |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for Operations-data brukes til å fylle ut rapporter i Workforce Metrics-innholdspakken. Tabellen nedenfor viser enhetene som innholdspakken er basert på.

| Enhet                            | Innhold                                                                                                   | Relasjoner med andre enheter                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalenderforskyvninger for å dele opp rapporter                                                                          | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Workforce\_Company                | Selskaper til å filtrere rapporter etter                                                                             | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_Compensation           | Lønnssats og frekvens over tid                                                                           | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_CurrentCompensation    | Lønnssats og frekvens per gjeldende dato                                                              | Workforce\_Company Workforce\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Stillinger per gjeldende dato, tilsvarende fulltidsekvivalent (FTE), ledige stillinger og ledig-til-besatt-stillinger | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                                               |
| Workforce\_CurrentWorker          | Arbeidere fra og med gjeldende dato, alder og antall ansatte                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit                                            |
| Workforce\_Date                   | Dager, uker, måneder og år.                                                                             | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Workforce\_Demographics           | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Employment             | Startdato, sluttdato og overgangsdato                                                                  | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_GeographicLocation     | By, fylke, postnummer og delstat eller område                                                           | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Job                    | Funksjon, type og tittel                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| Workforce\_PastPositionAssignment | Tilordningsårsak, startdato, sluttdato og jobb                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_Performance            | Vurdering, beskrivelse og vurderingsmodell                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_PersonSkill            | Nivå og ferdighet                                                                                            | Workforce\_Skill                                                                                                                                                                                                                                                                                                                 |
| Workforce\_PersonSkillAnalysis    | Sertifisert, nivå og ferdighet                                                                                | Workforce\_Skill Workforce\_WorkerName                                                                                                                                                                                                                                                                                           |
| Workforce\_Position               | Avdeling, FTE, plassering, stillingstype og tittel                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | Stillinger over tid, FTE og jobb                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | Fornavn, etternavn og fullt navn                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Skill                  | Kompetanse, kompetansetype og vurdering                                                                              | Workforce\_PersonSkill Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| Workforce\_TerminatedWorker       | Fratrådte arbeidere, avslutningsdato, tittel, stilling og jobb                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Ikrafttredelsesdato, fordelsalternativ, fordelsplan og fordelstype                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerName             | Fornavn, etternavn og fullt navn                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| Workforce\_WorkerTitle            | Tittel og ansiennitetsdato                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Arbeidere over tid, antall ansatte, firma og stilling                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdspakken. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen CompensationandBenefits.pbix fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette innholdspakken. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





