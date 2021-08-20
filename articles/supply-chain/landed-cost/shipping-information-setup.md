---
title: Konfigurasjon av forsendelsesinformasjon
description: Dette emnet beskriver hvordan du definerer forsendelsesinformasjon for modulen Netto innkjøpspris.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 4760a87bdcf0f109d5f78dae289446efa12bf359e7fe4b4beb0a983f68d95f34
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758622"
---
# <a name="shipping-information-setup"></a>Konfigurasjon av forsendelsesinformasjon

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du definerer forsendelsesinformasjon for modulen **Netto innkjøpspris**.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Beskrivelse av varer

Beskrivelser av varer hjelper til med å identifisere en sjøreise, forsendelsescontainer eller last og varene i den. Du kan velge en beskrivelse av varer i forsendelsescontainerens topptekst eller i foliotoppteksten.

Hvis du vil jobbe med varebeskrivelser, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Beskrivelse av varer**. Der kan du vise, åpne, opprette og slette poster for beskrivelser av varer. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Beskrivelse av varer | Angi et unikt identifikasjonsnavn/-nummer for varetypen som skal bruke denne beskrivelsen. |
| beskrivelse | Angi en beskrivelse av varetypen i denne kategorien. |

## <a name="vessels"></a><a name="vessels"></a>Fartøy

Et fartøy er det unike navn på et skip eller transportmiddel som brukes av et forsendelsesfirma eller byrå. Når du oppretter en sjøreise, må du alltid velge eller legge inn et transportmiddel for sjøreisen. Hvis du ofte bruker de samme transportmidlene, kan du gjøre det raskere og enklere å opprette en ny sjøreise ved å opprette en transportmiddelpost for hver av dem. Dermed gir du brukerne muligheten til å velge transportmidlet fra en liste i stedet for å oppgi navnet eller nummeret manuelt hver gang.

Hvis du vil arbeide med transportmidler, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Transportmidler**. Der kan du vise, åpne, opprette og slette poster for transportmidler. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Fartøy | Angi et unikt identifikasjonsnavn/-nummer for skipet som skal brukes til å transportere varer på en sjøreise. |
| beskrivelse | Angi en beskrivelse av transportmidlet. Denne beskrivelsen identifiserer vanligvis navnet på skipet og forsendelsesfirmaet/-agenten. |
| Leveringsmiddel | Velg leveringsmåten som for eksempel transportmidlet bruker (for eksempel _Lufttransport_, _Sjøtransport_ eller _Togtransport_). |

## <a name="exporters"></a>Eksportører

Hver eksportørpost identifiserer en leverandør eller eksportør som kan defineres som leverandøren for en sjøreise. Eksportøren kan knyttes til en sjøreise og brukes til rapportering.

Hvis du vil arbeide med eksportører, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Eksportører**. Der kan du vise, åpne, opprette og slette poster for eksportører. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Eksportør | Angi et unikt identifikasjonsnavn/-nummer for eksportøren av varer som blir transportert på en sjøreise. |
| beskrivelse | Angi en beskrivelse av eksportøren. Denne beskrivelsen identifiserer det fulle navnet på forsendelsesfirmaet/-agenten. |

## <a name="commodity-codes"></a>Artikkelkoder

Du bruker varekoder til å bidra med tollidentifikasjon og beregning av tollsatser for varer på en sjøreise. Du kan velge varekoder på siden **Frigitte produkter**.

Hvis du vil arbeide med varekoder, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Varekoder**. Der kan du vise, åpne, opprette og slette poster for varekoder. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Artikkelkode | Angi en unik kode for denne typen vare. |
| beskrivelse | Angi en beskrivelse av varetypen. |

## <a name="customs-description"></a>Tollbeskrivelse

Tollbeskrivelser hjelper med å identifisere varer for tollformål. Du kan velge en tollbeskrivelse på siden **Frigitte produkter** eller på bestillingslinjer.

Hvis du vil arbeide med tollbeskrivelser, går du til **Netto innkjøpspris \> Oppsett av forsendelsesinformasjon \> Tollbeskrivelse**. Der kan du vise, åpne, opprette og slette poster for tollbeskrivelser. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Tollbeskrivelse | Angi en unik kode for denne typen tollklassifikasjon. Ofte vil denne koden være den offisielle beskrivelsen som formidles av en tollmyndighet for beskrivelsen og den kvalitative verdien av varene. |
| beskrivelse | Angi en beskrivelse av tollklassifikasjonen. |
