---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (15. november 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462108"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>Hva er nytt eller endret i Dynamics 365 Talent – Core HR (15. november 2018)

**Build 8.1.2045**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.

## <a name="other-changesfixes"></a>Andre endringer/reparasjoner

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Kan ikke endre den ansattes gjeldende stilling til en fremtidig åpen stilling

En endring er gjort for å aktivere stillingsoverføringer når stillingen bare er tilgjengelig i fremtiden. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Stillingen vises ikke når du oppretter en ny ansatt

En endring er gjort for å vise alle ledige stillinger som er tilgjengelige for tilordningen, når du ansetter nye personer i Talent. Dette inkluderer historiske stillinger eller om stillingene er fremtidig daterte. Stillinger vises nå på riktig måte basert på startdatoen for ansettelsen. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Avslutningsdatoen vises basert på brukerinnstillinger

Har gjort en endring i listen over tidligere ansatte for å ta hensyn til alle tidssoneforskyvninger for den foretrukne tidssonen for ansatte når du viser avslutningsdatoen.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Koblinger til Arbeidselementer som er tilordnet til meg viser ikke riktig informasjon

Med denne endringer vil navigasjon til detaljene i de individuelle arbeidselementene i listen vise riktig informasjon for det valgte elementet. Dette problemet oppstod bare med avanserte sikkerhetsalternativer.


## <a name="known-issue"></a>Kjent problem

- **Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene. 
- **Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket. Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert. (Dette problemet vil bli løst i neste plattformoppdatering.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]