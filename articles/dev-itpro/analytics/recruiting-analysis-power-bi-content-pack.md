---
title: Recruiting-innhold for Power BI
description: "Dette emnet beskriver Recruiting-innhold for Power BI. Det forklarer hvordan du kan få tilgang til rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 42d7b94e655799596f478e7592a17437b336099e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="recruiting-power-bi-content"></a>Recruiting-innhold for Power BI

[!include[banner](../includes/banner.md)]

Dette emnet beskriver **Recruiting**-innhold for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vil **Recruiting** for Power BI-innholdet vises i arbeidsområdet **Rekrutteringsstyring**. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Rapporter og visuelle effekter i arbeidsområdet Rekrutteringsstyring
Arbeidsområdet **Rekrutteringsstyring** inneholder en **Analyse**-kategori. Denne kategorien inneholder det innebygde Power BI-innholdet for rekruttering. Innholdet består av en oversiktskategori og flere kategorier som inneholder detaljer. Tabellen nedenfor beskriver rapportene i hver kategori.

| Rapporter               | Innhold |
|----------------------|----------|
| Oversikt over rekruttering | Sammendrag av andre rapporter |
| Søkeranalyse   | Totalt antall søkere, søkere etter jobb, søkerkilder, forholdet mellom kvinnelige og mannlige søkere, og søkere etter sted |
| Søkerstatus     | Søkere etter type, status og søkerstatus |
| Rekrutteringsanalyse  | Netto ansettelsesforhold, gjennomsnittlig antall dager for å ansette, prosent av dårlige ansettelser, rekrutteringskostnader, antall rekrutteringsprosjekter, ansettelse til brukt og søkere vs. ledige stillinger etter rekrutteringsprosjekt |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Tabellen nedenfor viser enhetene som **Recruiting**-innholdet for Power BI er basert på.

| Enhet               | Innhold                                                         | Relasjoner med andre enheter |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Søker            | Søkere, ansatte søkere, netto ansettelsesforhold og kostnader          | Navn på søker, selskap, kalenderforskyvning, dato, geografisk plassering, demografi, jobb, media, rekrutteringsprosjekt |
| Søkernavn       | Søkerens fornavn, etternavn og fulle navn                   | Søker, ansatt søker, avsluttet søker |
| Kalenderforskyvning      | Kalenderforskyvninger for å dele opp rapporter                                | Søker, ansatt søker, avsluttet søker |
| Firma              | Selskaper til å filtrere rapporter etter                                   | Søker, ansatt søker, avsluttet søker |
| Dato                 | Dager, uker, måneder og år.                                   | Søker, ansatt søker, avsluttet søker |
| Demografi         | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status         | Søker, ansatt søker, avsluttet søker |
| Ansatt søker   | Søkeren, ytelse, startdato og søkertype           | Selskap, kalenderforskyvning, dato, geografisk plassering, navn på søker, ansettelse, ytelse, jobb, media, rekrutteringsprosjekt |
| Ansettelse           | Startdato, sluttdato og overgangsdato                        | Søker, ansatt søker, avsluttet søker |
| Geografisk plassering  | By, fylke, postnummer og delstat eller område                 | Søker, ansatt søker, avsluttet søker |
| Jobb                  | Funksjon, type og tittel                                        | Søker, ansatt søker, avsluttet søker |
| Medier                | Søkerkilde                                             | Søker, ansatt søker, avsluttet søker |
| Ytelse          | Vurdering, beskrivelse og vurderingsmodell                            | Søker, ansatt søker, avsluttet søker |
| Rekrutteringsprosjekt  | Prosjektbeskrivelse, prosjektstatus og stillinger                | Søker, ansatt søker, avsluttet søker |
| Avsluttet søker | Avsluttede søkere, årsak, ytelse og avslutningsdato | Selskap, kalenderforskyvning, dato, geografisk plassering, ytelse, demografi, ansettelse, media, rekrutteringsprosjekt, navn på søker |

Disse enhetene ble brukt til å opprette beregnede mål. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdet. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen Recruiting.pbix fra Microsoft Dynamics Lifecycle Services (LCS). Denne filen er standarddatamodellen som ble brukt til å opprette innholdet. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

