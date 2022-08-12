---
title: Power BI-innholdet Ansattutvikling
description: Denne artikkelen beskriver Power BI-innholdet om ansattutvikling.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 45c93589385cea399b71b2ad33c87a5c805124d5
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206551"
---
# <a name="employee-development-power-bi-content"></a>Power BI-innholdet Ansattutvikling

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver **Ansattutvikling** Microsoft Power BI-innhold.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet
Rapporter som er inkludert i Power BI-innholdet **Ansattutvikling**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                        | Innhold |
|-------------------------------|----------|
| Oversikt over ansattutvikling | Sammendrag av andre rapporter |
| Kompetanseanalyse, ansatt       | Ansattes kompetansetyper og ansattkompetanse etter type |
| Analyse av ansattes kompetansenivå | Ansattes kompetansenivåer etter avdeling, ansatte etter kompetansenivå og kompetansetype, og laveste og høyeste nivå per kompetanse |
| Kompetanseprofil                 | Kompetanseprofil for den valgte ansatte |
| Kompetanseanalyse                | Kompetanse etter type og vurdering |
| Analyse av ytelsesvurdering   | Ansatte etter laveste og høyeste vurdering etter jobb, ansattvurderinger etter avdeling, ansatte etter vurdering og stillingstype og høyeste og laveste vurdering etter stilling |
| Resultatanalyse, ansatt | Ansattvurderinger for valgte vurdering etter leder |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

| Enhet                   | Innhold                                                                                                   | Relasjoner med andre enheter |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenderforskyvning          | Kalenderforskyvninger for å dele opp rapporter                                                                          | Tidligere stillingstilordning, stillingstrend, trend for ansatt, fratrådt ansatt |
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
| Jobb                      | Funksjon, type og tittel                                                                                  | Gjeldende ansatt, gjeldende stilling, trend for ansatt, jobb– foretrukket kompetanse, tidligere stillingstilordning, stillingstrend, tidligere ansatte |
| Jobb, foretrukket kompetanse      | Viktighet, vurdering, kompetanse og kompetansenivå                                                                 | Jobb |
| Kompetanseanalyse, ansatt  | Sertifisert, nivå, nivådato og kompetanse                                                                    | Ansattnavn, kompetanse |
| Ytelse              | Vurdering, beskrivelse og vurderingsmodell                                                                      | Gjeldende ansatt, gjeldende stilling, trend for ansatt, jobb– foretrukket kompetanse, tidligere stillingstilordning, stillingstrend, tidligere ansatte |
| Kompetanse                    | Kompetanse, kompetansetype og vurdering                                                                              | Kompetanseanalyse – ansatt, Jobb – foretrukket kompetanse |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
