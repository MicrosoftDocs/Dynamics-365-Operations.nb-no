---
title: Power BI-innholdet Fordeler
description: Dette emnet beskriver Power BI-innholdet Fordeler.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: e9bc69c31a5a5bfb31ba5a8d583cfb36c09fe25f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754524"
---
# <a name="benefits-power-bi-content"></a>Power BI-innholdet Fordeler

[!include [banner](../includes/banner.md)]

Dette emnet beskriver innholdet i **Fordeler** Microsoft Power BI. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet
Power BI-innholdet **Fordeler** vises i arbeidsområdet **Fordelsbehandling** hvis du bruker et av følgende produkter:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet
Rapportene som er inkludert i Power BI-innholdet **Fordeler**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                      | Innhold                                                                                       |
|-----------------------------|------------------------------------------------------------------------------------------------|
| Oversikt over fordelsregistrering | Planer med flest og færrest registreringer, registrering etter ansattgruppe og valgte alternativer for fordelsplan |
| Ansattfordeler           | Ansattregistrering etter valgt fordel                                                        |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Følgende data brukes til å fylle ut rapportene i Power BI-innholdet **Fordeler**. Denne tabellen viser enhetene som innholdet er basert på.

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