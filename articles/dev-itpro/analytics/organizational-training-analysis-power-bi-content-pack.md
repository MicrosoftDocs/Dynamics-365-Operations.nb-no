---
title: "Organisasjonsopplæring-innhold for Power BI"
description: "Dette emnet beskriver Finance and Operations - Organisasjonsopplæringsinnhold for Power BI. Det forklarer hvordan du kan få tilgang til innholdspakken, og beskriver datamodellen og enhetene som brukes til å bygge innholdspakken."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e49d9af8b8bd8d5edb977c49742861199c6964fd
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="organizational-training-power-bi-content"></a>Organisasjonsopplæring-innhold for Power BI

[!include[banner](../includes/banner.md)]


Dette emnet beskriver Finance and Operations - Organisasjonsopplæringsinnhold for Power BI. Det forklarer hvordan du kan få tilgang til innholdspakken, og beskriver datamodellen og enhetene som brukes til å bygge innholdspakken.

<a name="accessing-the-content-pack"></a>Tilgang til innholdspakken
--------------------------

Du kan finne Organisasjonsopplæring-innholdspakken i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og kobler den til Microsoft Dynamics 365 for Finance and Operations-data, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til Finance and Operations-dataene dine, viser rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innholdspakken, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter          | Innhold                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursanalyse | Registrering etter plassering, deltakere på kurset etter status og registreringsliste |
| Kurstyper    | Kurstyper etter kompetanse                                                       |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Finance and Operations-data brukes til å fylle ut rapporter i Organisasjonsopplæring-innholdspakken. Tabellen nedenfor viser enhetene som innholdspakken er basert på.

| Enhet                    | Innhold                                                         | Relasjoner med andre enheter                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Kalenderforskyvninger for å dele opp rapporter                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Selskaper til å filtrere rapporter etter                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Kurs, beskrivelse, instruktørnavn, sted, rom og status | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Agenda, kurs og start- og sluttidspunktene                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Navn, status, jobb og registreringsdato                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Kompetanse, kompetansetype og nivå                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Dager, uker, måneder og år.                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Startdato, sluttdato og overgangsdato                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Funksjon, type og tittel                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Posisjon, tittel og fulltidsekvivalente (FTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Fornavn, etternavn og fullt navn                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Tittel og ansiennitetsdato                                         | Training\_CourseAttendees                                                                                                                                                                          |

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdspakken. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen Training.pbix fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette innholdspakken. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





