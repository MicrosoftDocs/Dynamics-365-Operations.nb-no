---
title: Arbeidere uten ansettelse
description: Arbeidere som ikke har en fremtidig, aktiv eller historisk ansettelse i organisasjonen, vises i skjemaet Arbeidere uten ansettelse.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71cb119e533e64b14badf65f55e8c4d5aa4c4b2f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356590"
---
# <a name="workers-without-employment"></a>Arbeidere uten ansettelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbeidere som ikke har en fremtidig, aktiv eller historisk ansettelse i organisasjonen, vises i skjemaet **Arbeidere uten ansettelse**. Arbeidere med denne statusen kan vises når du importerer arbeidere uten en ansettelsespost, eller når du sletter en arbeiders ansettelse via **Arbeidere > Ansettelseshistorikk**.

Som standard er skjemaet **Arbeidere uten ansettelse** tilgjengelig for følgende roller:

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