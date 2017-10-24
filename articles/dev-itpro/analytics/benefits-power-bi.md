---
title: Power BI-innholdet Fordeler
description: "Dette emnet beskriver Power BI-innholdet Fordeler. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
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
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e650047473136d1aaf455e96f9d7c63a426563f
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="benefits-power-bi-content"></a>Power BI-innholdet Fordeler

[!include[banner](../includes/banner.md)]

Dette emnet beskriver Microsoft Power BI-innholdet **Fordeler**. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
Power BI-innholdet **Fordeler** vises i arbeidsområdet **Fordelsbehandling** hvis du bruker et av følgende produkter:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet
Rapporter som er inkludert i Power BI-innholdet **Fordeler**, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                       | Innhold                                                                                       |
|------------------------------|------------------------------------------------------------------------------------------------|
| Oversikt over fordelsregistrering  | Planer med flest og færrest registreringer, registrering etter ansattgruppe og valgte alternativer for fordelsplan |
| Ansattfordeler            | Ansattregistrering etter valgt fordel                                                        |
                                                                                             
Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Utvide Power BI-innholdet
Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Finance and Operations, gode analyser. Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere innholdspakkene på Power BI.com-leieren for analyse.

Du kan finne Power BI-innholdet **Fordeler** i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

>[!NOTE]
>PBIX-filene som er tilgjengelige i Lifecycle Services, gjelder bare for Finance and Operations.

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

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdet. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen PBIX-filen fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette innholdet. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

