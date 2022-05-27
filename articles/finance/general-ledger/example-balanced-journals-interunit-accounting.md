---
title: Balanserte journaler for interenhetsregnskap
description: Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden.
author: kweekley
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38a7d88602dcd0121eb331dab8bf35a815287f8c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712321"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Balanserte journaler for interenhetsregnskap

[!include [banner](../includes/banner.md)]

Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden. 

Hvis kontooppføringer ikke balanseres på nivået for verdiene for finansdimensjonen, blir det automatisk opprettet tilleggskontooppføringer for å balansere journalen. Disse kontooppføringene bruker posteringstypene **Enhetsintern - debet** og **Enhetsintern - kredit** på siden **Kontoer for automatiske transaksjoner** for å bestemme hovedkontoen. For eksempel Forretningsenhet, som er det andre segmentet i finanskontoen, er valgt som den balanserende finansdimensjonen, og følgende regnskapsoppføringer skal opprettes.

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 D |
| 6100 – NY – OU\_249  | 100,00 D |
| 2100 – MSP – OU\_256 | 200,00 K |

I dette tilfellet bestemmes følgende saldoer: 

-   For Forretningsenhet MSP = 100,00 K
-   For Forretningsenhet NY = 100,00 D

Følgende regnskapsoppføringer opprettes derfor automatisk for å balansere journalen på nivået til finansdimensjonsverdiene.

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| (Enhetsintern debet) – MSP – OU\_256 | 100,00 D |
| (Enhetsintern kredit) – NY – OU\_249 | 100,00 K |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
