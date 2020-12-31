---
title: Analysere innkommende dokumenter i Excel-format
description: Dette emnet gir informasjon om utforming av elektronisk rapportering (ER)-formater for å analysere innholdet i innkommende Microsoft Excel-filer.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6e27806d3b94eb485705cec539a4849b81fbba91
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685793"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Analysere innkommende dokumenter i Excel-format

[!include[banner](../includes/banner.md)]

Du kan utforme elektronisk rapportering (ER)-formater for å analysere innkommende Microsoft Excel-filer som representerer data i Microsoft Excel-arbeidsbøker (XLSX-formatfiler). Du kan deretter bruke innholdet fra disse filene til å oppdatere programdata. Dette er nyttig hvis du:

- Utformer ny modell og nytt format og ønsker å teste dem under kjøring. I så fall vil Excel simulere de faktiske programdataene.
- Behandle data utenfor programmet i Excel og ønsker å importere disse dataene for å sende en bestemt rapport.

Hvis du vil vite mer om denne funksjonen, kan du spille av oppgaveveiledningene **ER Importer data fra en Microsoft Excel-fil (del 1: Utforme format)** og **ER Importer data fra en Microsoft Excel-fil (del 2: Importere data)** (deler av 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)-forretningsprosessen). Disse oppgaveveiledningene går gjennom hvordan den innkommende Excel-filen kan analyseres ved hjelp av ER-formatet for å importere informasjon fra innkommende dokumenter og oppdatere programdata. Du kan laste ned oppgaveveiledningsfilene fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).

Last ned følgende filer for å fullføre oppgaveveiledningene som er nevnt over.

| Innholdsbeskrivelse                         | Fil                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Innkommende fil i .XLSX-format - mal    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Innkommende fil i .XLSX-format - eksempeldata | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Hvis du ennå ikke har spilt av følgende oppgaveveiledning [ER Opprette nødvendige konfigurasjoner for å importere data fra en ekstern fil](./tasks/er-required-configurations-import-data.md) i det gjeldende Finance and Operations-programmet, kan du laste ned følgende fil.

| Innholdsbeskrivelse    | Fil                                                            |
|------------------------|-----------------------------------------------------------------|
| ER-modellkonfigurasjon | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
