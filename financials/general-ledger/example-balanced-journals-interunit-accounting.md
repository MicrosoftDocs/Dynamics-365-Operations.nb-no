---
title: Balanserte journaler for interenhetsregnskap
description: "Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8b6fda79222905b0df211a0b944aca9e4dc76850
ms.lasthandoff: 03/31/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>Balanserte journaler for interenhetsregnskap

[!include[banner](../includes/banner.md)]


Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden. 

Hvis kontooppføringer ikke balanseres på nivået for verdiene for finansdimensjonen, blir det automatisk opprettet tilleggskontooppføringer for å balansere journalen. Disse kontooppføringene bruker posteringstypene **Enhetsintern - debet**og ** Enhetsintern - kredit** på siden **Kontoer for automatiske transaksjoner** for å bestemme hovedkontoen. For eksempel avdeling, som er det andre segmentet i finanskontoen, er valgt som den balanserende finansdimensjonen, og følgende regnskapsoppføringer skal opprettes.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 D |
| 6100 – NY – OU\_249  | 100,00 D |
| 2100 – MSP – OU\_256 | 200,00 K |

I dette tilfellet bestemmes følgende saldoer: 

-   For avdeling MSP = 100,00 K
-   For avdeling NY = 100,00 K

Følgende regnskapsoppføringer opprettes derfor automatisk for å balansere journalen på nivået til finansdimensjonsverdiene.

|                                   |           |
|-----------------------------------|-----------|
| (Enhetsintern debet) – MSP – OU\_256 | 100,00 D |
| (Enhetsintern kredit) – NY – OU\_249 | 100,00 K |






