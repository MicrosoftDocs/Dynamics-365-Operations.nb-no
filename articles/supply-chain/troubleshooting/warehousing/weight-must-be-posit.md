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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776782"
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
