---
title: Bølge er ikke kvalifisert for opprydding
description: Bølge er ikke kvalifisert for opprydding
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924333"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Bølge er ikke kvalifisert for opprydding

Feilkode: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Bølgen %1 er ikke berettiget til opprydding.

Bølgedataene kan ikke ryddes opp.  

## <a name="cause"></a>Årsak

Bølgen behandles i øyeblikket, som angitt ved en av følgende betingelser:

- Feltet **Bølgestatus** er satt til *Utfører*.
- Når du velger **Satsvis jobb** i **Bølge**-gruppen i kategorien **Bølge** i handlingsruten, er ikke **Status**-feltet angitt til *Avsluttet*, *Feil* eller *Avbrutt*. Derfor er det for øyeblikket en satsvis jobb som kjører.

## <a name="resolution"></a>Oppløsning

I handlingsruten i kategorien **Bølge** i **Bølge**-gruppen velger du **Satsvis jobb**, og følger deretter ett av disse trinnene:

- Hvis **Status**-feltet er satt til *Utfører*: I handlingsruten i kategorien **Satsvis jobb**, i **Satvis jobb**-gruppen, velger du **Vis oppgaver**. Du kan følge fremdriften ved å oppdatere siden **Satsvise oppgaver**.
- Hvis **Status**-feltet ikke er satt til *Utfører*: I handlingsruten i kategorien **Satsvis jobb**, i **Funksjoner**-gruppen, velger du **Endre status**. I feltet **Velg ny status** velger du *Venter*. Velg deretter **OK**.
