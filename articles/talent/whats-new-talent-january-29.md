---
title: Hva er nytt eller endret i Dynamics 365 Talent (31. januar 2019)
description: Dette emnet beskriver funksjoner som er nye eller endret i Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690058"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (31. januar 2019)

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

**Build 8.1.2128**

## <a name="core-hr-changes"></a>Core HR-endringer

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Fridager tatt på fraværskort vurderer ikke fraværsplandatoer
For fraværsplaner som ikke kjøres i henhold til et kalenderår, viser **Tatt**-kortet nå fravær som er tatt i det plandefinerte fraværsåret. For eksempel hvis organisasjonens fraværsår er 1. juni til og med 30. mai og en ansatt har tatt tre dager fri i desember, viser **Tatt**-kortet 3 dager for 15. januar. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Avsetningsbeløp samsvarer ikke med datogrunnlag for nivå
Nye alternativer er lagt til for permisjon og fravær (**Personale**-parametere) for å gjøre det mulig for kunder å fastsette når ansattes dato for måneder med jobberfaring er gyldig. I noen organisasjoner er datoen på slutten av måneden, men det kan være starten av neste måned for andre. En organisasjon kan for eksempel belønne ansatte med fri 31. desember, mens en annen gir fri 1. januar. Med dette alternativet kan du velge når belønningen skal skje. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Arbeideransettelseshandlinger står fast i "Arbeidsflyt fullført"-tilstand
Endringer er gjort for å løse et problem der et lite antall arbeidsprosesser ble fullført med en "Arbeidsflyt fullført"-status. Nye arbeidsflyter skal nå flyttes til en "Fullført"-tilstand når arbeidsflyten er fullført. Arbeidsflyter med en Arbeidsflyt fullført-status blir overført til en feilstatus for å tillate oppdatering eller fjerning hvis nødvendig. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]