---
title: Power BI-innholdet Kompensasjon og fordeler
description: Dette emnet beskriver Power BI-innholdet Kompensasjon og fordeler.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 69149f55371f64b4907f6040e9de03843fc11717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687212"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Power BI-innholdet Kompensasjon og fordeler

[!include [banner](../includes/banner.md)]

Dette emnet beskriver Power BI-innholdet Kompensasjon og fordeler. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til dataene dine, viser rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innholdspakken, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                     | Innhold                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Analyse av Kompensasjon og fordeler | Times- og lønnsansatte etter firma, gjennomsnittlig timelønn, gjennomsnittlig lønnsbasert lønn, ansatte etter ansettelsestype og planregistrering |
| Ansattfordeler          | Ansattregistrering etter valgt fordel                                                                                               |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Programdataene brukes til å fylle ut rapporter i innholdspakken Kompensasjon og fordeler. Tabellen nedenfor viser enhetene som innholdspakken er basert på.

| Enhet                            | Innhold                                                                                                   | Relasjoner med andre enheter |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalenderforskyvninger for å dele opp rapporter                                                                          | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker |
| Workforce\_Company                | Selskaper til å filtrere rapporter etter                                                                             | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Compensation           | Lønnssats og frekvens over tid                                                                           | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_CurrentCompensation    | Lønnssats og frekvens per gjeldende dato                                                              | Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Stillinger per gjeldende dato, tilsvarende fulltidsekvivalent (FTE), ledige stillinger og ledig-til-besatt-stillinger | Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentWorker          | Arbeidere fra og med gjeldende dato, alder og antall ansatte                                                         | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_Date                   | Dager, uker, måneder og år.                                                                             | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Demographics           | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Employment             | Startdato, sluttdato og overgangsdato                                                                  | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_GeographicLocation     | By, fylke, postnummer og delstat eller område                                                           | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Job                    | Funksjon, type og tittel                                                                                  | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PastPositionAssignment | Tilordningsårsak, startdato, sluttdato og jobb                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Vurdering, beskrivelse og vurderingsmodell                                                                      | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Position               | Avdeling, FTE, plassering, stillingstype og tittel                                                        | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | Stillinger over tid, FTE og jobb                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Fornavn, etternavn og fullt navn                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Skill                  | Kompetanse, kompetansetype og vurdering                                                                              | |
| Workforce\_TerminatedWorker       | Fratrådte arbeidere, avslutningsdato, tittel, stilling og jobb                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Ikrafttredelsesdato, fordelsalternativ, fordelsplan og fordelstype                                             | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerName             | Fornavn, etternavn og fullt navn                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTitle            | Tittel og ansiennitetsdato                                                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTrend            | Arbeidere over tid, antall ansatte, firma og stilling                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |
