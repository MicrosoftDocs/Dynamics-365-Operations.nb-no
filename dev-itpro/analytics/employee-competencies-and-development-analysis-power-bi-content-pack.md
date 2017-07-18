---
title: Kompetanser og utvikling for ansatt-innhold for Power BI
description: "Dette emnet beskriver FInance and Operations - Kompetanser og utvikling for ansatt-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: f5b3c180f0a9d60fa5d4d8398daf79a14da2d6f4
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="employee-competencies-and-development-power-bi-content"></a>Kompetanser og utvikling for ansatt-innhold for Power BI

[!include[banner](../includes/banner.md)]


Dette emnet beskriver FInance and Operations - Kompetanser og utvikling for ansatt-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken.

<a name="accessing-the-content-pack"></a>Tilgang til innholdspakken
--------------------------

Du kan finne innholdspakken for Kompetanser og utvikling for ansatt i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og kobler den til Microsoft Dynamics 365 for Finance and Operations-data, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til Finance and Operations-dataene dine, viser rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innholdspakken, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                            | Innhold                                               |
|-----------------------------------|--------------------------------------------------------|
| Analyse av Kompetanser og utvikling | Kompetansetyper for teammedlem og kompetanse for teammedlem etter type |
| Kompetanseprofil                     | Kompetanseprofil for den valgte ansatte                |
| Kompetanseanalyse                    | Kompetanse etter type og vurdering                              |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Finance and Operations-data brukes til å fylle ut rapporter i innholdspakken for Kompetanser og utvikling for ansatt. Tabellen nedenfor viser enhetene som innholdspakken er basert på.

| Enhet                            | Innhold                                                                                                   | Relasjoner med andre enheter                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalenderforskyvninger for å dele opp rapporter                                                                          |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Company                | Selskaper til å filtrere rapporter etter                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Compensation           | Lønnssats og frekvens over tid                                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_CurrentCompensation    | Lønnssats og frekvens per gjeldende dato                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Stillinger per gjeldende dato, tilsvarende fulltidsekvivalent (FTE), ledige stillinger og ledig-til-besatt-stillinger | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | Arbeidere fra og med gjeldende dato, alder og antall ansatte                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Workforce\_Date                   | Dager, uker, måneder og år.                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Demographics           | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                                                   |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Employment             | Startdato, sluttdato og overgangsdato                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_GeographicLocation     | By, fylke, postnummer og delstat eller område                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Job                    | Funksjon, type og tittel                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | Viktighet, vurdering, kompetanse og kompetansenivå                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Workforce\_PastPositionAssignment | Tilordningsårsak, startdato, sluttdato og jobb                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_Performance            | Vurdering, beskrivelse og vurderingsmodell                                                                      |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PersonSkill            | Nivå, nivådato og kompetanse                                                                               | Workforce\_Skill                                                                                                                                                                                                                                                                                        |
| Workforce\_PersonSkillAnalysis    | Sertifisert, nivå, nivådato og kompetanse                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | Avdeling, FTE, plassering, stillingstype og tittel                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | Stillinger over tid, FTE og jobb                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | Fornavn, etternavn og fullt navn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Skill                  | Kompetanse, kompetansetype og vurdering                                                                              |                                                                                                                                                                                                                                                                                                         |
| Workforce\_TerminatedWorker       | Fratrådte arbeidere, avslutningsdato, tittel, stilling og jobb                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Workforce\_WorkerName             | Fornavn, etternavn og fullt navn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_WorkerTitle            | Tittel og ansiennitetsdato                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Arbeidere over tid, antall ansatte, firma og stilling                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdspakken. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen CompetenciesandDevelopment.pbix fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette innholdspakken. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





