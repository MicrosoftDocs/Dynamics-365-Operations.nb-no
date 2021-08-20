---
title: Power BI-innholdet Kompetanser og utvikling for ansatt
description: Dette emnet beskriver Power BI-innholdet om kompetanser og utvikling for ansatt.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 572f6bcfa202995d90080e1a31476122f7ec23d71214d5ff0dd44ed919859c57
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726315"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI-innholdet Kompetanser og utvikling for ansatt

[!include [banner](../includes/banner.md)]

Dette emnet beskriver Power BI-innholdet om kompetanser og utvikling for ansatt. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til dataene dine, viser rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innholdspakken, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                            | Innhold                                               |
|-----------------------------------|--------------------------------------------------------|
| Analyse av Kompetanser og utvikling | Kompetansetyper for teammedlem og kompetanse for teammedlem etter type |
| Kompetanseprofil                     | Kompetanseprofil for den valgte ansatte                |
| Kompetanseanalyse                    | Kompetanse etter type og vurdering                              |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Programdata brukes til å fylle ut rapporter i innholdspakken for Kompetanser og utvikling for ansatte. Tabellen nedenfor viser enhetene som innholdspakken er basert på.

| Enhet                            | Innhold                                                                                                   | Relasjoner med andre enheter |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalenderforskyvninger for å dele opp rapporter                                                                          | |
| Workforce\_Company                | Selskaper til å filtrere rapporter etter                                                                             | |
| Workforce\_Compensation           | Lønnssats og frekvens over tid                                                                           | |
| Workforce\_CurrentCompensation    | Lønnssats og frekvens per gjeldende dato                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Stillinger per gjeldende dato, tilsvarende fulltidsekvivalent (FTE), ledige stillinger og ledig-til-besatt-stillinger | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Arbeidere fra og med gjeldende dato, alder og antall ansatte                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | Dager, uker, måneder og år.                                                                             | |
| Workforce\_Demographics           | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                                                   | |
| Workforce\_Employment             | Startdato, sluttdato og overgangsdato                                                                  | |
| Workforce\_GeographicLocation     | By, fylke, postnummer og delstat eller område                                                           | |
| Workforce\_Job                    | Funksjon, type og tittel                                                                                  | |
| Workforce\_JobPreferredSkill      | Viktighet, vurdering, kompetanse og kompetansenivå                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | Tilordningsårsak, startdato, sluttdato og jobb                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Vurdering, beskrivelse og vurderingsmodell                                                                      | |
| Workforce\_PersonSkill            | Nivå, nivådato og kompetanse                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | Sertifisert, nivå, nivådato og kompetanse                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Avdeling, FTE, plassering, stillingstype og tittel                                                        | |
| Workforce\_PositionTrend          | Stillinger over tid, FTE og jobb                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Fornavn, etternavn og fullt navn                                                                       | |
| Workforce\_Skill                  | Kompetanse, kompetansetype og vurdering                                                                              | |
| Workforce\_TerminatedWorker       | Fratrådte arbeidere, avslutningsdato, tittel, stilling og jobb                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | Fornavn, etternavn og fullt navn                                                                       | |
| Workforce\_WorkerTitle            | Tittel og ansiennitetsdato                                                                                   | |
| Workorce\_WorkerTrend             | Arbeidere over tid, antall ansatte, firma og stilling                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]