---
title: "Opplæringsinnhold for Power BI"
description: "Dette emnet beskriver opplæringsinnholdet i Power BI. Det forklarer hvordan du kan få tilgang til rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a3f28d21a7e73d3ad462c5cc37198dd2b6f5f8af
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="learning-power-bi-content"></a>Opplæringsinnhold for Power BI

[!include[banner](../includes/banner.md)]

Dette emnet beskriver Microsoft Power BI-innholdet **Opplæring**. Det forklarer hvordan du kan få tilgang til innholdet, og beskriver datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold

Hvis du bruker oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations versjon 1611,Enterprise edition, kan du finne Power BI-innholdet **Opplæring** i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet

Rapporter som er inkludert i Power BI-innholdet **Opplæring**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                | Innhold |
|-----------------------|----------|
| Oversikt over opplæring     | Sammendrag av andre rapporter |
| Kursanalyse       | Registrering etter plassering, deltakere etter status, kurs etter type per firma og kursfremmøte etter jobb |
| Registreringsanalyse | Registreringsliste |
| Kurstyper          | Kurstyper etter kompetanse |
| Instruktøranalyse   | Forholdet mellom kurs og instruktører, antall instruktører, kurs etter instruktør, kurs per instruktør og kursagenda etter instruktør |
| Kurs som tilbys       | Liste over kurs |
| Kursutforming        | Kursagenda |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

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

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdet. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen PBIX-filen fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette innholdet. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

