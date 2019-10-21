---
title: Power BI-innholdet Opplæring
description: Dette emnet beskriver Power BI-innholdet Opplæring.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f4752c4b61c396db82e5804292607f142bfbe691
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184330"
---
# <a name="learning-power-bi-content"></a>Power BI-innholdet Opplæring

[!include [banner](../includes/banner.md)]

Dette emnet beskriver Microsoft Power BI-innholdet **Opplæring**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet

Rapportene som er inkludert i Power BI-innholdet **Opplæring**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                | Innhold |
|-----------------------|----------|
| Oversikt over opplæring     | Sammendrag av andre rapporter |
| Kursanalyse       | Registrering etter plassering, deltakere etter status, kurs etter type per firma og kursfremmøte etter jobb |
| Registreringsanalyse | Registreringsliste |
| Kurstyper          | Kurstyper etter kompetanse |
| Instruktøranalyse   | Forholdet mellom kurs og instruktører, antall instruktører, kurs etter instruktør, kurs per instruktør og kursagenda etter instruktør |
| Kurs som tilbys       | Liste over kurs |
| Kursutforming        | Kursagenda |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

Følgende data brukes til å fylle ut rapportene i Power BI-innholdet **Opplæring**. Denne tabellen viser enhetene som innholdet er basert på.

| Enhet           | Innhold                                                         | Relasjoner med andre enheter |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalenderforskyvning  | Kalenderforskyvninger for å dele opp rapporter                                | Kursagenda, kursdeltakere |
| Firma          | Selskaper til å filtrere rapporter etter                                   | Kursagenda, kursdeltakere |
| Kurs           | Kurs, beskrivelse, instruktørnavn, sted, rom og status | Kursagenda, kursdeltakere, kurskompetanse |
| Kursagenda    | Agenda, kurs og start- og sluttidspunktene                          | Firma, kalenderforskyvning, dato, kurs |
| Kursdeltakere | Navn, status, jobb og registreringsdato                         | Firma, kalenderforskyvning, dato, kurs, demografi, ansettelse, kurs, ansattnavn, ansattittel, jobb, stilling |
| Kurskompetanse     | Kompetanse, kompetansetype og nivå                                     | Kurs |
| Dato             | Dager, uker, måneder og år.                                   | Kursagenda, kursdeltakere |
| Demografi     | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status         | Kursagenda, kursdeltakere |
| Ansettelse       | Startdato, sluttdato og overgangsdato                        | Kursagenda, kursdeltakere |
| Jobb              | Funksjon, type og tittel                                        | Kursagenda, kursdeltakere |
| Posisjon         | Posisjon, tittel og fulltidsekvivalente (FTE)                  | Kursagenda, kursdeltakere |
| Navn på ansatt    | Fornavn, etternavn og fullt navn                             | Kursdeltakere |
| Ansattittel   | Tittel og ansiennitetsdato                                         | Kursdeltakere |