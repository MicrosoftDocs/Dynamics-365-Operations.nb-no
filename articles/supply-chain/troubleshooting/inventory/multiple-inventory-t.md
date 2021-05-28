---
title: Flere lagertransaksjoner for partinumre når Ved fysisk oppdatering er deaktivert
description: Det opprettes flere lagertransaksjoner etter at du har justert en bestillingslinje for varer der alternativet Ved fysisk oppdatering for partinummergruppen er satt til Nei.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026793"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Flere lagertransaksjoner for partinumre når Ved fysisk oppdatering er deaktivert

KB-nummer: 4613390

## <a name="symptoms"></a>Symptomer

Det opprettes flere lagertransaksjoner etter at du har justert en bestillingslinje for varer der alternativet **Ved fysisk oppdatering** for partinummergruppen er satt til *Nei*.

Når du oppretter en vare der alternativet **Ved fysisk oppdatering** for partinummergruppen er satt til *Nei*, oppretter systemet automatisk et nytt partinummer hvis du endrer et innkjøpslinjeantall og lagrer bestillingssiden.

## <a name="resolution"></a>Oppløsning

Innstillingen **Ved fysisk oppdatering** for partinummergrupper fungerer på følgende måte:

- Når alternativet er satt til *Ja*, opprettes det bare nye partinumre etter en fysisk oppdatering (for eksempel når varer sendes eller mottas).
- Når alternativet er satt til *Nei*, opprettes det et nytt partinummer hver gang det foretas en gjeldende oppdatering (for eksempel når et nytt antall legges til i en bestilling).
