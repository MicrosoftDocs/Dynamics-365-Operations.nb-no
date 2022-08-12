---
title: Power BI-innholdet Rekruttering
description: Denne artikkelen beskriver Power BI-innholdet Rekruttering.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom:
- "263934"
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.form: HcmRecruitmentWorkspace
ms.openlocfilehash: 3bce9b165623ed415a0902d3f369a5deef56e8b6
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205800"
---
# <a name="recruiting-power-bi-content"></a>Power BI-innholdet Rekruttering

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver Microsoft Power BI-innholdet **Rekruttering**. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet
Power BI-innholdet **Rekruttering** vises i **Rekrutteringsstyring**-arbeidsområdet.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Rapporter og visuelle effekter i arbeidsområdet Rekrutteringsstyring
Arbeidsområdet **Rekrutteringsstyring** inneholder en **Analyse**-kategori. Denne fanen inneholder det innebygde Power BI-innholdet for rekruttering. Innholdet består av en oversiktskategori og flere kategorier som inneholder detaljer. Tabellen nedenfor beskriver rapportene i hver kategori.

| Rapporter               | Innhold |
|----------------------|----------|
| Oversikt over rekruttering | Sammendrag av andre rapporter |
| Søkeranalyse   | Totalt antall søkere, søkere etter jobb, søkerkilder, forholdet mellom kvinnelige og mannlige søkere, og søkere etter sted |
| Søkerstatus     | Søkere etter type, status og søkerstatus |
| Rekrutteringsanalyse  | Netto ansettelsesforhold, gjennomsnittlig antall dager for å ansette, prosent av dårlige ansettelser, rekrutteringskostnader, antall rekrutteringsprosjekter, ansettelse til brukt og søkere vs. ledige stillinger etter rekrutteringsprosjekt |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Tabellen nedenfor viser enhetene som Power BI-innholdet **Rekruttering** er basert på.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
