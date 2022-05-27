---
title: Arbeidere uten ansettelse
description: Arbeidere som ikke har en fremtidig, aktiv eller historisk ansettelse i organisasjonen, vises på siden Arbeidere uten ansettelse.
author: twheeloc
ms.date: 11/03/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3b2d5d470e780c708941fd3d08eae1a042b4c03
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689810"
---
# <a name="workers-without-employment"></a>Arbeidere uten ansettelse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbeidere som ikke har en fremtidig, aktiv eller historisk ansettelse i organisasjonen, vises på siden **Arbeidere uten ansettelse**. Arbeidere av denne typen kan vises når du importerer arbeidere uten en ansettelsespost, eller når du sletter en arbeiders ansettelse via **Arbeidere \> Ansettelseshistorikk**.

Som standard er siden **Arbeidere uten ansettelse** tilgjengelig for følgende roller:

- Personalassistent
- Personalsjef
- Rekrutterer
- Kompensasjons og fordelsansvarlig
- Lønnsadministrator
- Lønnsansvarlig
- Opplæringsleder

I listne **Arbeidere uten ansettelse** kan du slette personene som er oppført. Som standard gis dette privilegiet til personalassistentrollen. Du kan gi denne rettigheten til andre roller ved hjelp av følgende trinn:

1. Velg **Systemadministrasjon**, og velg deretter **Sikkerhetskonfigurasjon**.

2. I kategorien **Rettigheter** filtrerer du **Rettigheter**-listen til **Vedlikehold arbeidere**.

   [![Filterrettigheter-liste.](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. I **Referanser**-kolonnen velger du **Vis menyelementer**.

4. I **Vis menyelementer** velger du **HcmWorkersWithoutEmployment**.

   [![Velg skjema.](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Angi **Slett**-tillatelsen som du skal **innvilge**.

6. Velg kategorien **Upubliserte objekter**.

7. Velg **Publiser alle**.

   [![Publiser endringer.](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
