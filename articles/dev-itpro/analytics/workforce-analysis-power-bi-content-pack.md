---
title: Workforce Metrics-innhold for Power BI
description: "Dette emnet beskriver Workforce Metrics-innholdet for Power BI. Det forklarer hvordan du kan få tilgang til rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorkforceWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 8ff4eb80eeb47a72fc1ac91ddc4bdfccebc4c0c6
ms.contentlocale: nb-no
ms.lasthandoff: 12/19/2017

---

# <a name="workforce-metrics-power-bi-content"></a>Workforce Metrics-innhold for Power BI

[!include[banner](../includes/banner.md)]

Dette emnet beskriver **Workforce Metrics**-innholdet for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
**Workforce Metrics**-innholdet for Power BI vises i arbeidsområdet **Personaladministrasjon** hvis du bruker ett av disse produktene:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 
- Microsoft Dynamics 365 for Talent

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
Tabellen nedenfor viser målene som vises for hver rapport.

| Rapporter                                           | Mål                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mål for personer                                   | Sammendrag av andre rapporter                                                                                                                           |
| Arbeidsstokken analyse firmanavn, avdeling, sted | Antall ansatte etter selskap, etter avdeling, etter sted og totalt antall ansatte                                                                                                                           |
| Analysejobb for antall ansatte, trinn, leder            | Antall ansatte etter jobb, etter trinn, etter leder og totalt antall ansatte                                                                                                                                      |
| Trendanalyse for antall ansatte                         | Antall ansatte inneværende år sammenlignet med fjoråret etter selskap og rullerende antall ansatte for de siste 12 månedene                                                                                                                        |
| FTE-analyse                                     | Total heltidsekvivalent (FTE), total tilordnet FTE, FTE etter avdeling, FTE for de siste 12 månedene og FTE etter jobb |
| Demografi for arbeidsstyrken                           | Antall ansatte etter alder, kjønn, etnisitet, veteranstatus, ekteskapelig status, antall heltidsstudenter, gjennomsnittlig fartstid, gjennomsnittsalder, forholdet mellom kvinnelige og mannlige ansatte og språk som ansatte snakker |
| Stillingsanalyse                                | Åpne stillinger etter avdeling, ledig-til-besatt-stillinger, aktiv-til-inaktive-stillinger og stillinger etter avdeling                                                                                                   |
| Avgangsanalyse                               | Avgang inneværende år sammenlignet med fjoråret, avgang, ansatte som slutter etter alder og kjønn, gjennomsnittlig fartstid for ansatte som slutter denne måneden og ansatte som slutter etter årsak                                                                   |
| Personer etter avdeling                             | Ansatte med et personalnummer etter avdeling, stilling og start- og sluttdatoer for tildeling                                                                                                                       |
| Ansiennitetsanalyse                               | Liste over gjennomsnittlig fartstid, gjennomsnittlig antall år med arbeidserfaring etter selskap og ansiennitet                                                                                                                                                              |
| Ansattes jubileer                           | Jubileer denne måneden, jubileer neste måned, ansatte etter arbeidserfaring og jubileer, arbeidserfaring etter avdeling                                                                                                                                                                    |
| Ansattes fødselsdager                               | Fødselsdager denne måneden, fødselsdager neste måned, ansattes fødselsdager og fødselsdager etter måned og avdeling                                                                                                                                                                    |
| Masseansettelsesprosjekter                               | Totalt antall masseansettelsesprosjekter, masseansettelsesprosjekter etter status, masseansettelsesprosjekter etter avdeling og eier, masseansettelsesprosjekter etter jobb og masseansettelsesprosjekter                                                                                                                                                                    |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Pass på at du laster ned **Workforce Metrics**-innholdet for Power BI som gjelder for versjonen av Microsoft Dynamics 365 som du bruker.

>[!NOTE]
>PBIX-filene som er tilgjengelige i Lifecycle Services, gjelder bare for Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Tabellen nedenfor viser enhetene som innholdet er basert på.

| Enhet                   | Innhold                                                                            | Relasjoner med andre enheter |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Kalenderforskyvning          | Kalenderforskyvninger for å dele opp rapporter                                                   | Tidligere stillingstilordning, stillingstrend, trend for ansatt, fratrådt ansatt |
| Firma                  | Selskaper til å filtrere rapporter etter                                                      | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Gjeldende stilling         | Stillinger per gjeldende dato, FTE, ledige stillinger og ledig-til-besatt-stillinger | Jobb, stilling |
| Gjeldende ansatt         | Arbeidere fra og med gjeldende dato, alder og antall ansatte                                  | Firma, geografisk plassering, ansattnavn, rapporterer til, ansattittel, demografi, jobb, ansettelse, stilling |
| Dato                     | Dager, uker, måneder og år.                                                      | Tidligere stillingstilordning, stillingstrend, fratrådt ansatt, trend for ansatt |
| Demografi             | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                            | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Ansettelse               | Startdato, sluttdato og overgangsdato                                           | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Geografisk plassering      | By, fylke, postnummer og delstat eller område                                    | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Jobb                      | Funksjon, type og tittel                                                           | Gjeldende plassering, gjeldende ansatt |
| Tidligere stillingstilordning | Tilordningsårsak, startdato, sluttdato og jobb                                    | Kalenderforskyvning, dato, jobb, stilling |
| Posisjon                 | Avdeling, FTE, plassering, stillingstype og tittel                                 | Gjeldende plassering, gjeldende ansatt |
| Stillingstrend           | Stillinger over tid, FTE og jobb                                                   | Kalenderforskyvning, dato, jobb, stilling |
| Rapporter til               | Fornavn, etternavn og fullt navn                                                | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Tidligere ansatt      | Fratrådte arbeidere, avslutningsdato, tittel, stilling og jobb                      | Firma, geografisk plassering, ansattnavn, rapporterer til, kalenderforskyvning, dato, ansattittel, demografi, ansettelse, jobb, stilling |
| Navn på ansatt            | Fornavn, etternavn og fullt navn                                                | Gjeldende arbeider, fratrådt ansatt, trend for ansatt |
| Ansattittel           | Tittel og ansiennitetsdato                                                            | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Trend for ansatt           | Arbeidere over tid, antall ansatte, firma og stilling                                 | Firma, geografisk plassering, ansattnavn, rapporterer til, kalenderforskyvning, dato, ansattittel, demografi, ansettelse, jobb |
| Masseansettelsesprosjekt        | Antall masseansettelsesprosjekter, prosjekteier og prosjektstatus                     | Firma, masseansettelseslinje |
| Masseansettelseslinje           | Avdeling, ansettelsestype og stilling                                           | Dato, jobb, masseansettelsesprosjekt |



