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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719557"
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
