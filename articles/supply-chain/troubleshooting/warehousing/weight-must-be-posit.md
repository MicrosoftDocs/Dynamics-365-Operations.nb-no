---
title: Vekten må være positiv
description: Vekten må være positiv
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924309"
---
# <a name="weight-must-be-positive"></a>Vekten må være positiv

Feilkode: WeightMustBePositive

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Vekten må være positiv.

## <a name="cause"></a>Årsak

**Bruttovekt**-feltet er satt til *0* (null) eller en negativ verdi.

## <a name="resolution"></a>Oppløsning

Hvis du vil angi en vekt, gjør du ett av følgende.

- Angi en verdi i **Bruttovekt**-feltet. Velg deretter en enhet fra rullegardinlisten.
- Velg **Hent systemvekt** for å beregne **bruttovektverdien**.
