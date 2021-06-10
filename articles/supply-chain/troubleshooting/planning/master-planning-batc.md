---
title: Du kan ikke filtrere hovedplanleggingselementer etter de tilknyttede dekningsgruppeverdiene
description: Du kan ikke filtrere hovedplanleggingselementer etter de tilknyttede dekningsgruppeverdiene.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049483"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Du kan ikke filtrere hovedplanleggingselementer etter de tilknyttede dekningsgruppeverdiene

KB-nummer: 4612572

## <a name="symptoms"></a>Symptomer

Du vil filtrere varene som skal inkluderes i en satsvis jobb for hovedplanlegging, basert på verdiene til relaterte poster fra varedekningstabellen. (Du vil for eksempel filtrere varene etter **Leverandør** og/eller **Dekningsgruppe**). Med filteroppsettet for den satsvise jobben kan du opprette en kobling fra **Varer**-tabellen til **Varedekning**-tabellen og deretter angi feltverdier fra varedekningstabellen i spørringen. Når du har fullført dette oppsettet, oppretter imidlertid systemet planlagte bestillinger for hele varedekningen, ikke bare for varene som samsvarer med de angitte feltverdiene fra varedekningstabellen.

## <a name="resolution"></a>Løsning

Filteret for den satsvise jobben kan bare filtrere på varer. Selv om du kan legge til en kobling i **Varedekning**-tabellen, vil ikke filterinnstillingene du gjør mot tabellen, påvirke resultatet av spørringen. Ved kjøretid kjører systemet planlegging for alle dekningsgruppene og alle variasjonene de filtrerte varene har. Når en vare allerede er inkludert i kjøringen, vil ikke dekningsgrupper som er inkludert i varefilteret, påvirke planleggingsresultatet.
