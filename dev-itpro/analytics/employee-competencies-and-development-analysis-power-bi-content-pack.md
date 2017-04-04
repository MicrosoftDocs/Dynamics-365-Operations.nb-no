---
title: "Ansattes kompetanser og utvikling strømmen BI-innhold"
description: "Dette emnet beskriver Dynamics-365 for operasjoner - ansattes kompetanser og utvikling strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i innhold pack, og gir informasjon om en datamodell og enheter som ble brukt til å lage innhold pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Ansattes kompetanser og utvikling strømmen BI-innhold

Dette emnet beskriver Dynamics-365 for operasjoner - ansattes kompetanser og utvikling strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i innhold pack, og gir informasjon om en datamodell og enheter som ble brukt til å lage innhold pack.

<a name="accessing-the-content-pack"></a>Tilgang til innhold pack
--------------------------

Du kan finne den ansattes kompetanser og utvikling innhold pack i delte aktiva biblioteket i Microsoft Dynamics Lifecycle tjenester (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innhold pack og koble den til din Microsoft Dynamics-365 for operasjoner data, se [strømmen BI-innhold i LCS fra Microsoft og partnere på](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innhold pack
Når du har koblet innhold pack til din Dynamics 365 for operasjoner data, vise rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du lære mer om det på den [veiledende læring side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innhold pack har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                            | Innhold                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetanse og utvikling analyse | Team medlem ferdighetstyper og ferdigheter av team medlem av typen |
| Kompetanseprofil                     | Kompetanseprofil for den valgte ansatt                |
| Kompetanseanalyse                    | Kompetanse etter type og klassifisering                              |

Du kan filtrere diagrammer og fliser på disse rapportene og feste diagrammer og fliser på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filter og PIN-koden i strømmen BI, se [opprette og konfigurere en instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for operasjoner data brukes til å fylle ut rapportene i den ansattes kompetanser og utvikling innhold pack. Tabellen nedenfor viser enhetene som innhold pack er basert på.

| Enhet                            | Innhold                                                                                                   | Relasjoner med andre enheter                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arbeidsstyrken\_CalendarOffset         | Kalenderen forskyvninger stykke rapporter                                                                          |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_firma                | Selskaper til å filtrere rapporter med                                                                             |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_kompensasjon           | Lønnssatsen og ofte over tid                                                                           |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_CurrentCompensation    | Lønnssatsen og frekvens per gjeldende dato                                                              | Arbeidsstyrken\_Company arbeidsstyrke\_CurrentCompensation arbeidsstyrke\_demografi arbeidsstyrke\_jobb arbeidsstyrke\_posisjon                                                                                                                                                                                            |
| Arbeidsstyrken\_CurrentPosition        | Stillinger per gjeldende dato, tilsvarende fulltidsekvivalente (FTE), åpne stillinger og åpne til fylt stillinger | Arbeidsstyrken\_jobb arbeidsstyrke\_posisjon                                                                                                                                                                                                                                                                      |
| Arbeidsstyrken\_CurrentWorker          | Arbeidere fra og med gjeldende dato, alder og arbeidsstokken                                                         | Arbeidsstyrken\_Company arbeidsstyrke\_kompensasjon arbeidsstyrke\_GeographicLocation arbeidsstyrke\_ytelse arbeidsstyrke\_PersonSkill arbeidsstyrke\_WorkerName arbeidsstyrke\_ReportsToWorkerName arbeidsstyrke\_WorkerTitle arbeidsstyrke\_demografi arbeidsstyrke\_jobb arbeidsstyrke\_ansettelse arbeidsstyrke\_posisjon                     |
| Arbeidsstyrken\_dato                   | Dager, uker, måneder og år                                                                             |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_demografi           | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                                                   |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_ansettelse             | Startdato, sluttdato og dato for overgang                                                                  |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_GeographicLocation     | By, fylke, postnummer-koden og delstat / region                                                           |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_jobb                    | Funksjons-, type- og tittel                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_JobPreferredSkill      | Nivå for viktighet, vurdering, kompetanse og ferdigheter                                                                 | Arbeidsstyrken\_ferdighet arbeidsstyrke\_jobb                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_PastPositionAssignment | Tildeling årsak, startdato, sluttdato og jobb                                                           | Arbeidsstyrken\_ClaendarOffset arbeidsstyrke\_dato arbeidsstyrke\_jobb arbeidsstyrke\_posisjon                                                                                                                                                                                                                            |
| Arbeidsstyrken\_ytelse            | Vurdering, beskrivelse og vurderingsmodellen                                                                      |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_PersonSkill            | Nivå, nivå dato og kompetanse                                                                               | Arbeidsstyrken\_ferdighet                                                                                                                                                                                                                                                                                        |
| Arbeidsstyrken\_PersonSkillAnalysis    | Dato for sertifiserte, nivåer, nivå og kompetanse                                                                    | Arbeidsstyrken\_WorkerName arbeidsstyrke\_ferdighet                                                                                                                                                                                                                                                                  |
| Arbeidsstyrken\_posisjon               | Avdeling, FTE, plassering, stillingstypen og tittel                                                        |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_PositionTrend          | Posisjoner over tid, FTE og jobb                                                                          | Arbeidsstyrken\_CalendarOffset arbeidsstyrke\_dato arbeidsstyrke\_jobb arbeidsstyrke\_posisjon                                                                                                                                                                                                                            |
| Arbeidsstyrken\_ReportsToWorkerName    | Fornavn, Etternavn og fullt navn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_ferdighet                  | Kompetanse, kompetanse og klassifisering                                                                              |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_TerminatedWorker       | Avsluttet arbeidere, sluttet dato, tittel, plassering og jobb                                             | Arbeidsstyrken\_Company arbeidsstyrke\_kompensasjon arbeidsstyrke\_GeographicLocation arbeidsstyrke\_ytelse arbeidsstyrke\_WorkerName arbeidsstyrke\_ReportsToWorkerName arbeidsstyrke\_CalendarOffset Workforces\_dato arbeidsstyrke\_WorkerTitle arbeidsstyrke\_demografi arbeidsstyrke\_ansettelse arbeidsstyrke\_jobb arbeidsstyrke\_posisjon |
| Arbeidsstyrken\_WorkerName             | Fornavn, Etternavn og fullt navn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Arbeidsstyrken\_WorkerTitle            | Tittel og ansiennitet                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Arbeidere over tid, arbeidsstokken, firmaet og posisjon                                                        | Arbeidsstyrken\_Company arbeidsstyrke\_kompensasjon arbeidsstyrke\_GeographicLocation arbeidsstyrke\_ytelse arbeidsstyrke\_WorkerName arbeidsstyrke\_ReportsToWorkerName arbeidsstyrke\_CalendarOffset Workforces\_dato arbeidsstyrke\_WorkerTitle arbeidsstyrke\_demografi arbeidsstyrke\_ansettelse arbeidsstyrke\_jobb                     |

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnet mål brukes deretter til å beregne viktige ytelsesindikatorer (KPIer) og rapporter som brukes i content pack. Hvis du vil ta med flere beregninger i rapporter og instrumentbord, kan du laste ned og endre filen CompetenciesandDevelopment.pbix fra LCS. Denne filen er standard datamodellen som ble brukt til å opprette innhold pack. Når du har gjort endringene, kan du opprette en organisatorisk innholdspakken og instrumentbord som inneholder informasjon som du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



