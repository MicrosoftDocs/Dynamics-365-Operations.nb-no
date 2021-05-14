---
title: Arbeid blokkeres ikke
description: Arbeid blokkeres ikke
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924210"
---
# <a name="work-isnt-blocked"></a>Arbeid er ikke sperret

Feilkode: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Arbeid med ID-en %1 er ikke blokkert.

## <a name="cause"></a>Årsak

Alternativet **Blokkert bølge** i bølgen er satt til *Nei*. Blokkering av arbeidet kan ikke oppheves, fordi det i øyeblikket ikke er blokkert.

## <a name="resolution"></a>Oppløsning

 Bare arbeid der alternativet **Blokkert bølge** er satt til *Ja*, kan oppheve blokkering.
