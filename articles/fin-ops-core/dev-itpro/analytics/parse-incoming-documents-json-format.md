---
title: Analysere innkommende dokumenter i JSON-format
description: Dette emnet beskriver hvordan du konfigurerer ER-formater (elektroniske rapporter) for å analysere innkommende dokumenter i JSON-format (JavaScript Object Notation).
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4e598dc15b619c2f6a0525ea18c371484ca26fa4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755160"
---
# <a name="parse-incoming-documents-in-json-format"></a>Analysere innkommende dokumenter i JSON-format

[!include[banner](../includes/banner.md)]

Du kan utforme ER-formater (elektronisk rapportering) for å analysere innkommende elektroniske dokumenter som representerer data i et tekstformat som er basert på JavaScript (med andre ord filer i JSON-format \[JavaScript Object Notation\]).

Hvis du vil ha mer informasjon om denne funksjonen, kan du laste ned filene i følgende tabell og deretter spille av oppgaveveiledningen «ER Opprette en formatkonfigurasjon for å importere data fra en ekstern JSON-fil». Denne oppgaveveiledningen viser hvordan et ER-format kan brukes til å analysere en innkommende JSON-fil for å oppdatere programdata.

| Stillingstittel                                  | Filnavn |
|----------------------------------------|-----------|
| ER-formatkonfigurasjon                | [Format for import av leverandørenes trans_JSON.xml](https://go.microsoft.com/fwlink/?linkid=874111) |
| Eksempel på innkommende fil i CSV-format | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Behov

Før du fullfører oppgaveveiledningen «ER Opprette en formatkonfigurasjon for å importere data fra en ekstern JSON-fil», må følgende krav oppfylles:

- Overordnede elementer i JSON-filen kan bare være objektelementer.
- Nestede elementer for et objekt bør være egenskapselementer, slik at du lager en gyldig JSON-struktur.
- JSON-matriser kan bare være nestede elementer i egenskapselementene for et objekt.
- JSON-matriser kan bare inneholde JSON-objekter. De kan ikke inneholde direkte strengverdier / numeriske verdier og nestede matriser. Elementer i disse matrisene analyseres i rekkefølge, slik de er angitt i formatet. Multiplisitet-innstillingene for hvert JSON-objekt blir vurdert.

Du må i tillegg fullføre oppgaveveiledningen [ER Opprette nødvendige konfigurasjoner for å importere data fra en ekstern fil](tasks/er-required-configurations-import-data.md) hvis du ikke allerede har fullført den. Last ned følgende file for å fullføre oppgaveveiledningen.

| Stillingstittel                  | Filnavn |
|------------------------|-----------|
| ER-modellkonfigurasjon | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]