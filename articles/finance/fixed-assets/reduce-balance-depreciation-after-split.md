---
title: Redusere saldoavskrivning etter en deling
description: Denne artikkelen beskriver metoden som brukes i anleggsmidler til å beregne avskrivning etter at et aktiva er delt, ved å bruke metoden for reduksjon av saldo.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 539967a9a73da91f6b49c1bb89f404267ae0a804
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883307"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Redusere saldoavskrivning etter en deling

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver metoden som brukes i anleggsmidler til å beregne avskrivning etter at et aktiva er delt til et annet aktiva, ved å bruke metoden for reduksjon av saldo. Avskrivningsåret som er konfigurert i aktivatablået, er regnskapsåret. Hvis du vil ha mer informasjon, kan du se [Redusere saldoavskrivning](reduce-balance-depreciation.md) og [Dele et anleggsmiddel](tasks/split-fixed-asset.md).

Hvis du deler et anleggsmiddel i løpet av en regnskapsperiode som er senere enn perioden da anleggsmidlet ble anskaffet, vil den reduserte saldoavskrivningen redegjøre for aktivaets netto bokførte verdi for fjoråret. Det vil også ta redegjøre for justeringstransaksjoner for anskaffelse og avskrivning som ble generert fra transaksjonen som delte opp aktivaet. Denne virkemåten forutsetter at aktivaet ble anskaffet i ett regnskapsår og delt i et senere regnskapsår. Beløpet som må avskrives for det opprinnelige aktivaet etter at delingen gjenspeiler aktivaets netto bokførte verdi før aktivaet ble delt, og justeringstransaksjonen for anskaffelse og avskrivning som ble postert for delingen.

Følgende betingelser gjelder for eksempel:

- Regnskapsperioden er fra 30. juni til 1. juli.
- Saldoverdiprosent er 18 prosent, og et aktiva anskaffes i juni 2019 til en anskaffelsespris på $10.000.
- Avskrivningen for det første regnskapsåret er lik $18.000, den månedlige avskrivningen er lik $150, og aktivaet blir deretter avskrevet til november 2019 med $738,75.
- I november 2019 deles 80 prosent av aktivaet med et anleggsmiddel.

[![Redusere saldoavskrivning etter en deling.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Beløpet som skal avskrives for det opprinnelige aktivaet, er $1822,25. Dette beløpet er lik netto bokført verdi før delingstransaksjonen posteres ($9 111,25), pluss anskaffelsesjusteringen som genereres under postering av delingstransaksjonen (-$8 000), pluss avskrivningsjusteringen som genereres i løpet av delingstransaksjonen ($711). Derfor er avskrivningen for det andre året (1 822,25 × 18 prosent) ÷ 12 = $27,33.

Beløpet som skal avskrives for det nye aktivaet i det første året er (8 000 × 18 prosent) ÷ 12 = $120.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
