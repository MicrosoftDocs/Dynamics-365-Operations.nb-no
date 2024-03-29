---
title: Power BI-innholdet Opplæring
description: Denne artikkelen beskriver Power BI-innholdet Opplæring.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a7aca9e47ed26dcb4ef7f4b9aee72987e2d8fdd2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273967"
---
# <a name="learning-power-bi-content"></a>Power BI-innholdet Opplæring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver Microsoft Power BI-innholdet **Opplæring**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet

Rapportene som er inkludert i Power BI-innholdet **Opplæring**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                | Innhold |
|-----------------------|----------|
| Oversikt over opplæring     | Sammendrag av andre rapporter |
| Kursanalyse       | Registrering etter plassering, deltakere etter status, kurs etter type per firma og kursfremmøte etter jobb |
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
