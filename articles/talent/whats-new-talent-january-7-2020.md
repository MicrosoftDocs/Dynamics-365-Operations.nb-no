---
title: Hva er nytt eller endret i Dynamics 365 Talent (7. januar 2020)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462121"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Hva er nytt eller endret i Dynamics 365 Talent (7. januar 2020)

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2697. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Kan ikke slette arbeidere som ikke har ansettelsesposter – (386157)

Denne endringen legger til et slettealternativ i skjemaet **Arbeidere uten ansettelse**. Arbeidere vises i dette skjemaet når det ikke finnes fremtidige, aktive eller historiske ansettelsesforhold for arbeideren. I denne versjonen er sletting bare aktivert for systemansvarlige. I neste ukes versjon vil imidlertid sikkerhet bli oppdatert slik at alle brukere med rollen personalassistent kan fjerne ansatte uten ansettelser. Du kan også utføre disse endringene manuelt ved å følge fremgangsmåten nedenfor.

1. Gå til **Sikkerhetskonfigurasjon**.
2. I kategorien **Rettigheter** filtrerer du **Rettigheter**-listen til **Vedlikehold arbeidere**.
3. I **Referanser**-kolonnen velger du **Vis menyelementer**.
4. I **Vis menyelementer** velger du **HcmWOrkersWithoutEmployment**.
5. Angi **Slett**-tillatelsen som skal gis.
6. Velg kategorien **Upubliserte objekter**.
7. Velg **Publiser alle**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]