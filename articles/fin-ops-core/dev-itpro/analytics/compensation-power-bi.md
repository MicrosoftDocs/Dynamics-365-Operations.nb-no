---
title: Power BI-innholdet Kompensasjon
description: Dette emnet beskriver Power BI-innholdet Kompensasjon. Det forklarer hvordan du får tilgang til rapporter og gir informasjon om datamodellen som brukes.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCompensationWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 549111dab1b6d3b66567801ae787a680a04b18e20e286e1a59d1ab388bf2a4f7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763602"
---
# <a name="compensation-power-bi-content"></a>Power BI-innholdet Kompensasjon

[!include [banner](../includes/banner.md)]

Dette emnet beskriver Microsoft Power BI-innholdet i **Kompensasjon**. Det forklarer hvordan du kan få tilgang til rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet
Power BI-innholdet **Kompensasjon** vises i arbeidsområdet **Kompensasjonsstyring** hvis du bruker et av følgende produkter:

- Finance and Operations-apper
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet
Rapportene som er inkludert i Power BI-innholdet **Kompensasjon**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                     | Innhold |
|----------------------------|----------|
| Oversikt over kompensasjon      | Sammendrag av andre rapporter |
| Kompensasjonsanalyse      | Ansatte med timelønn og lønn etter firma, totalt antall ansatte etter kompensasjonsplanen, mannlige og kvinnelige ansatte etter kompensasjonsplan og ansattkompensasjon etter avdeling |
| Analyse av lønn i forhold til stilling      | Høyeste og laveste timelønn og lønn, stillinger med høyeste og laveste lønn, og heltids- og deltidsstillinger |
| Analyse av kompensasjonsplan | Ansattregistrering etter valgt fordel |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Følgende data brukes til å fylle ut rapportene i Power BI-innholdet **Kompensasjon**. Denne tabellen viser enhetene som innholdet er basert på.

| Enhet                   | Innhold                                                                                                   | Relasjoner med andre enheter |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenderforskyvning          | Kalenderforskyvninger for å dele opp rapporter                                                                          | Tidligere stillingstilordning, stillingstrend, trend for ansatt, fratrådt ansatt |
| Firma                  | Selskaper til å filtrere rapporter etter                                                                             | Gjeldende kompensasjon, gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Kompensasjon             | Lønnssats og frekvens over tid                                                                           | Gjeldende kompensasjon, gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Gjeldende kompensasjon     | Lønnssats og frekvens per gjeldende dato                                                              | Firma, kompensasjon, demografi, jobb, stilling |
| Gjeldende stilling         | Stillinger per gjeldende dato, tilsvarende fulltidsekvivalent (FTE), ledige stillinger og ledig-til-besatt-stillinger | Jobb, stilling |
| Gjeldende ansatt         | Arbeidere fra og med gjeldende dato, alder og antall ansatte                                                         | Firma, kompensasjon, geografisk plassering, ansattnavn, rapporterer til, ansattittel, demografi, jobb, ansettelse, stilling, fordeler |
| Dato                     | Dager, uker, måneder og år.                                                                             | Tidligere stillingstilordning, stillingstrend, fratrådt ansatt, trend for ansatt |
| Demografi             | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status                                                   | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Ansettelse               | Startdato, sluttdato og overgangsdato                                                                  | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Geografisk plassering      | By, fylke, postnummer og delstat eller område                                                           | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Jobb                      | Funksjon, type og tittel                                                                                  | Gjeldende plassering, gjeldende ansatt |
| Tidligere stillingstilordning | Tilordningsårsak, startdato, sluttdato og jobb                                                           | Kalenderforskyvning, dato, jobb, stilling |
| Posisjon                 | Avdeling, FTE, plassering, stillingstype og tittel                                                        | Gjeldende plassering, gjeldende ansatt |
| Stillingstrend           | Stillinger over tid, FTE og jobb                                                                          | Kalenderforskyvning, dato, jobb, stilling |
| Rapporterer til               | Fornavn, etternavn og fullt navn                                                                       | Gjeldende arbeider, fratrådt ansatt, trend for ansatt |
| Fratrådt ansatt      | Fratrådte ansatte, avslutningsdato, tittel, stilling og jobb                                           | Firma, kompensasjon, geografisk plassering, ansattnavn, rapporterer til, kalenderforskyvning, dato, ansattittel, demografi, jobb, ansettelse, jobb, stilling, fordeler |
| Fordeler                 | Ikrafttredelsesdato, fordelsalternativ, fordelsplan og fordelstype                                             | Gjeldende navn, fratrådt ansatt, trend for ansatt |
| Navn på ansatt            | Fornavn, etternavn og fullt navn                                                                       | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Ansattittel           | Tittel og ansiennitetsdato                                                                                   | Gjeldende ansatt, fratrådt ansatt, trend for ansatt |
| Trend for ansatt           | Arbeidere over tid, antall ansatte, firma og stilling                                                        | Firma, kompensasjon, geografisk plassering, ansattnavn, rapporterer til, kalenderforskyvning, dato, ansattittel, demografi, ansettelse, jobb, fordeler |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]