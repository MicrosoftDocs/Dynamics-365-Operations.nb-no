---
title: "Organisatoriske opplæring strømmen BI-innhold"
description: "Dette emnet beskriver Dynamics-365 for operasjoner - organisatoriske opplæring strømmen BI-innhold. Det forklarer hvordan du får tilgang til innhold pack, og beskriver datamodell og enheter som ble brukt til å lage innhold pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organisatoriske opplæring strømmen BI-innhold

Dette emnet beskriver Dynamics-365 for operasjoner - organisatoriske opplæring strømmen BI-innhold. Det forklarer hvordan du får tilgang til innhold pack, og beskriver datamodell og enheter som ble brukt til å lage innhold pack.

<a name="accessing-the-content-pack"></a>Tilgang til innhold pack
--------------------------

Du kan finne den organisatoriske opplæring innhold pack i delte aktiva biblioteket i Microsoft Dynamics Lifecycle tjenester (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innhold pack og koble den til din Microsoft Dynamics-365 for operasjoner data, se [strømmen BI-innhold i LCS fra Microsoft og partnere på](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innhold pack
Når du har koblet innhold pack til din Dynamics 365 for operasjoner data, vise rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du lære mer om det på den [veiledende læring side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innhold pack har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter          | Innhold                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurset analyse | Registrering av plassering, deltakere på kurset ved status og Registreringsliste |
| Kurstyper    | Kurstyper etter kompetanse                                                       |

Du kan filtrere diagrammer og fliser på disse rapportene og feste diagrammer og fliser på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filter og PIN-koden i strømmen BI, se [opprette og konfigurere en instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for operasjoner data brukes til å fylle ut rapporter i organisasjonens opplæring innhold pack. Tabellen nedenfor viser enhetene som innhold pack er basert på.

| Enhet                    | Innhold                                                         | Relasjoner med andre enheter                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opplæring\_CalendarOffset  | Kalenderen forskyvninger stykke rapporter                                | Opplæring\_opplæring for CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Opplæring\_firma         | Selskaper til å filtrere rapporter med                                   | Opplæring\_opplæring for CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Opplæring\_kurs          | Kurset, beskrivelse, instruktør navn, plassering, plass og status | Opplæring\_opplæring for CourseAgenda\_opplæring for CourseAttendees\_CourseSkill                                                                                                                             |
| Opplæring\_CourseAgenda    | Agenda, kurs og start- og sluttidspunktene                          | Opplæring\_Company opplæring\_opplæring for CalendarOffset\_dato opplæring\_kurs                                                                                                                         |
| Opplæring\_CourseAttendees | Dato for navn, status, jobb og registrering                         | Opplæring\_Company opplæring\_CalendarOffset opplæring\_dato opplæring\_demografi opplæring\_ansettelse opplæring\_kurs opplæring\_opplæring for WorkerName\_WorkerTitle opplæring\_jobb opplæring\_posisjon |
| Opplæring\_CourseSkill     | Kompetanse, kompetanse og nivå                                     | Opplæring\_kurs                                                                                                                                                                                   |
| Opplæring\_dato            | Dager, uker, måneder og år                                   | Opplæring\_opplæring for CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Opplæring\_demografi    | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status         | Opplæring\_opplæring for CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Opplæring\_ansettelse      | Startdato, sluttdato og dato for overgang                        | Opplæring\_opplæring for CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Opplæring\_jobb             | Funksjons-, type- og tittel                                        | Opplæring\_opplæring for CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Opplæring\_posisjon        | Posisjon, tittel og tilsvarende fulltidsekvivalente (FTE)                  | Opplæring\_opplæring for CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Opplæring\_WorkerName      | Fornavn, Etternavn og fullt navn                             | Opplæring\_CourseAttendees                                                                                                                                                                          |
| Opplæring\_WorkerTitle     | Tittel og ansiennitet                                         | Opplæring\_CourseAttendees                                                                                                                                                                          |

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnet mål brukes deretter til å beregne viktige ytelsesindikatorer (KPIer) og rapporter som brukes i content pack. Hvis du vil ta med flere beregninger i rapporter og instrumentbord, kan du laste ned og endre filen Training.pbix fra LCS. Denne filen er standard datamodellen som ble brukt til å opprette innhold pack. Når du har gjort endringene, kan du opprette en organisatorisk innholdspakken og instrumentbord som inneholder informasjon som du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



