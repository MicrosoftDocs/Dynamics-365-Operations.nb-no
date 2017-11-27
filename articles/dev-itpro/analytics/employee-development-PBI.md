---
title: Power BI-innhold om ansattutvikling
description: "Dette emnet beskriver Power BI-innholdet om ansattutvikling. Det forklarer hvordan du kan få tilgang til rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c6a1125d56239f4370d6219a93988d50d402045e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="employee-development-power-bi-content"></a>Power BI-innhold om ansattutvikling

[!include[banner](../includes/banner.md)]

Dette emnet beskriver Power BI-innholdet om **ansattutvikling**. Det forklarer hvordan du kan få tilgang til rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold

Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vil du finne innholdspakken **Ansattutvikling** i Fellesskapsbiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og kobler den til dataene dine, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet
Rapporter som er inkludert i Power BI-innholdet **Ansattutvikling**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                        | Innhold |
|-------------------------------|----------|
| Oversikt over ansattutvikling | Sammendrag av andre rapporter |
| Kompetanseanalyse, ansatt       | Ansattes kompetansetyper og ansattkompetanse etter type |
| Analyse av ansattes kompetansenivå | Ansattes kompetansenivåer etter avdeling, ansatte etter kompetansenivå og kompetansetype, og laveste og høyeste nivå per kompetanse |
| Kompetanseprofil                 | Kompetanseprofil for den valgte ansatte |
| Kompetanseanalyse                | Kompetanse etter type og vurdering |
| Analyse av ytelsesvurdering   | Ansatte etter laveste og høyeste vurdering etter jobb, ansattvurderinger etter avdeling, ansatte etter vurdering og stillingstype og høyeste og laveste vurdering etter stilling  |
| Resultatanalyse, ansatt | Ansattvurderinger for valgte vurdering etter leder |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
| Enhet                   | Innhold                                                                                                   | Relasjoner med andre enheter |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenderforskyvning          | Kalenderforskyvninger for å dele opp rapporter                                                                          | Tidligere stillingstilordning, stillingstrend, trend for ansatt, fratrådt ansatt 
| Firma                  | Selskaper til å filtrere rapporter etter                                                                             | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Gjeldende stilling         | Stillinger per gjeldende dato, tilsvarende fulltidsekvivalent (FTE), ledige stillinger og ledig-til-besatt-stillinger | Jobb, stilling |
| Gjeldende ansatt         | Arbeidere fra og med gjeldende dato, alder og antall ansatte                                                         | Firma, geografisk plassering, ansattnavn, rapporterer til, ansattittel, demografi, jobb, ansettelse, stilling |
| Dato                     | Dager, uker, måneder og år.                                                                             | Tidligere stillingstilordning, stillingstrend, fratrådt ansatt, trend for ansatt |
| Demografi             | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                                                   | Gjeldende ansatt, fratrådt, ansatt, trend for ansatt |
| Ansettelse               | Startdato, sluttdato og overgangsdato                                                                  | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Geografisk plassering      | By, fylke, postnummer og delstat eller område                                                           | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Jobb                      | Funksjon, type og tittel                                                                                  | Gjeldende plassering, gjeldende ansatt |
| Tidligere stillingstilordning | Tilordningsårsak, startdato, sluttdato og jobb                                                           | Kalenderforskyvning, dato, jobb, stilling |
| Posisjon                 | Avdeling, FTE, plassering, stillingstype og tittel                                                        | Gjeldende plassering, gjeldende ansatt |
| Stillingstrend           | Stillinger over tid, FTE og jobb                                                                          | Kalenderforskyvning, dato, jobb, stilling |
| Rapporter til               | Fornavn, etternavn og fullt navn                                                                       | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Tidligere ansatt      | Fratrådte arbeidere, avslutningsdato, tittel, stilling og jobb                                             | Firma, geografisk plassering, ansattnavn, rapporterer til, kalenderforskyvning, dato, ansattittel, demografi, ansettelse, jobb, stilling |
| Navn på ansatt            | Fornavn, etternavn og fullt navn                                                                       | Gjeldende arbeider, fratrådt ansatt, trend for ansatt |
| Ansattittel           | Tittel og ansiennitetsdato                                                                                   | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Trend for ansatt           | Arbeidere over tid, antall ansatte, firma og stilling                                                        | Firma, geografisk plassering, ansattnavn, rapporterer til, kalenderforskyvning, dato, ansattittel, demografi, ansettelse, jobb |
| Jobb                      | Funksjon, type og tittel                                                                                      | Gjeldende ansatt, gjeldende stilling, trend for ansatt, jobb– foretrukket kompetanse, tidligere stillingstilordning, stillingstrend, tidligere ansatte |
| Jobb, foretrukket kompetanse      | Viktighet, vurdering, kompetanse og kompetansenivå                                                                 | Jobb |
| Kompetanseanalyse, ansatt  | Sertifisert, nivå, nivådato og kompetanse                                                                    | Ansattnavn, kompetanse |  
| Ytelse              | Vurdering, beskrivelse og vurderingsmodell                                                                      | Gjeldende ansatt, gjeldende stilling, trend for ansatt, jobb– foretrukket kompetanse, tidligere stillingstilordning, stillingstrend, tidligere ansatte |
|  Kompetanse                   | Kompetanse, kompetansetype og vurdering                                                                              | Kompetanseanalyse – ansatt, Jobb – foretrukket kompetanse |                                                                                                                        

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i Power-BI-innholdet. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen PBIX-filen fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette Power-BI-innhold. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

