---
title: Avrundingsbeløp for avskrivningsberegninger
description: Denne artikkelen omhandler feltet Avrundingsavskrivning som finnes på Tablåoppsett-sidene.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "308420"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Avrundingsbeløp for avskrivningsberegninger

[!include [banner](../includes/banner.md)]

Denne artikkelen omhandler feltet Avrundingsavskrivning som finnes på Tablåoppsett-sidene.

Avrundingsbeløp for avskrivning angis for hvert tablå. Avrundingsbeløp for avskrivning brukes i avskrivningsprofilen for anleggsmiddel som viser fremtidig avskrivning og verdi for anleggsmiddelet, også i avskrivningsforslag. Angi det laveste avskrivningsbeløpet som er tillatt for tablået. 

Uavhengig av avrundingen som er angitt, blir avskrivningsbeløpet i den siste avskrivningsperioden ikke avrundet. På slutten av siste avskrivningsperiode må verdien av anleggsmiddelet være 0 (null) eller skrapverdien, hvis skrapverdi brukes.

### <a name="example"></a>Eksempel

Avskrivning uten avrunding beregnes som 2 444,44. Som følgende tabell viser varierer beløpene som foreslås, avhengig av hvordan avrunding er satt opp.

| Avrundingsmetode | Avskrivningsbeløp |
|-----------------|---------------------|
| Avrunding 0,1    | 2 444,40            |
| Avrunding 1,00   | 2 444,00            |
| Avrunding 10,00  | 2 440,00            |
| Avrunding 100,00 | 2 400,00            |





