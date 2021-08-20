---
title: Power BI-innholdet Organisasjonsopplæring
description: Dette emnet beskriver Finance and Operations – Organisasjonsopplæringsinnhold for Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cd48c12ea3ea31904c437f678888a51e5381cfcfbeef0e1c709858b0c6cb857d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763554"
---
# <a name="organizational-training-power-bi-content"></a>Power BI-innholdet Organisasjonsopplæring

[!include [banner](../includes/banner.md)]

Dette emnet beskriver Finance and Operations – Organisasjonsopplæringsinnhold for Power BI.

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til dataene dine, viser rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innholdspakken, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter          | Innhold                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursanalyse | Registrering etter plassering, deltakere på kurset etter status og registreringsliste |
| Kurstyper    | Kurstyper etter kompetanse                                                       |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Programdata brukes til å fylle ut rapporter i Organisasjonsopplæring-innholdspakken. Tabellen nedenfor viser enhetene som innholdspakken er basert på.

| Enhet                    | Innhold                                                         | Relasjoner med andre enheter |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | Kalenderforskyvninger for å dele opp rapporter                                | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Company         | Selskaper til å filtrere rapporter etter                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Course          | Kurs, beskrivelse, instruktørnavn, sted, rom og status | Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill |
| Training\_CourseAgenda    | Agenda, kurs og start- og sluttidspunktene                          | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course |
| Training\_CourseAttendees | Navn, status, jobb og registreringsdato                         | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position |
| Training\_CourseSkill     | Kompetanse, kompetansetype og nivå                                     | Training\_Course |
| Training\_Date            | Dager, uker, måneder og år.                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Demographics    | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status         | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Employment      | Startdato, sluttdato og overgangsdato                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Job             | Funksjon, type og tittel                                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Position        | Posisjon, tittel og fulltidsekvivalente (FTE)                  | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_WorkerName      | Fornavn, etternavn og fullt navn                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | Tittel og ansiennitetsdato                                         | Training\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]