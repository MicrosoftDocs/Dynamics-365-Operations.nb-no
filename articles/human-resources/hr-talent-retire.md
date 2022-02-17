---
title: Foreldelse av Dynamics 365 Talent – Attract- og Onboard-apper
description: Dette emnet beskriver foreldelsen av Dynamics 365 Talent – Attract- og Onboard-apper.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: df33f35f66e356c3c2a99f0d81ebba1d0f34b5d9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069410"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Foreldelse av Dynamics 365 Talent: Attract- og Onboard-apper


I desember 2019 kunngjorde vi foreldelse av Dynamics 365 Talent – Attract- og Onboard-apper den 1. februar 2022, noe som har gitt kundene våre to år til å planlegge.

Hvis du vil ha mer informasjon om foreldelsen av disse appene, kan du se:
 - [Foreldelse av Dynamics 365 Talent – Attract- og Dynamics 365 Talent: Onboard-apper](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Bygge en mer vellykket arbeidsstyrke med Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Vi vil fortsette å støtte Dynamics 365 Human Resources, som vil hjelpe kundene våre med å få arbeidsstyrkeinnsikten som kreves for å bygge datadrevne ansattopplevelser på tvers av flere områder, for eksempel:

- Kompensasjon
- Fordeler
- Permisjon og fravær
- Samsvar
- Payroll
- Ytelse for tilbakemelding
- Opplæring og sertifisering
- Selvbetjeningsprogrammer

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Vanlige spørsmål om foreldelse av Dynamics 365 Talent-apper

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Hva er brukeropplevelsen for Dynamics 365 Talent – Attact- og Onboard-apper som starter 1. februar 2022?

Brukerne vil ikke være i stand til å bruke appene og blir sendt videre til en foreldelsesside.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Kan kundene fortsette å eksportere data for Dynamics 365 Talent – Attract- og Onboard-apper etter 1. februar 2022?
  
Nei, foreldelsen ble offentliggjort i desember 2019, og de nødvendige eksportfunksjonene var tilgjengelige til 1. februar 2022. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Vil kundens data relatert til Dynamics 365 Talent – Attract- og Onboard-apper i Dataverse bli slettet etter 1. februar 2022?

Nei, Dataverse-enhetenevil fortsatt være i kundens Microsoft Dataverse-miljø selv etter foreldelsen med mindre Human Capital Management Talent-løsningen slettes eller avinstalleres.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Jeg kjenner navnet på Talent-miljøet. Hvordan kan jeg se Attract- og Onboard-dataene i Dataverse?

1.  Logg på Power Apps: https://make.powerapps.com
2.  Velg miljøet der du vil se Attract- og Onboard-data.
3.  Gå til **Dataverse > Tabeller**. 
4.  Skriv inn "msdyn_" i **Søk**. Hvis du ser listen over tabeller som starter med "msdyn_" + tabellnavn (for eksempel msdyn_candidate), har du funnet miljøet med Attract- og Onboard-data.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Jeg kjenner ikke navnet på Talent-miljøet. Hvordan kan jeg finne miljøet som har dataene for Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-appen?

1)  Logg på Power Platform-administrasjonssenteret: https://admin.powerplatform.microsoft.com/
2)  Velg **Miljøer**.
3)  Velg et miljø som skal evalueres.
4)  Velg **Ressurser > Dynamics 365-apper**.
5)  Hvis du ser **HCM Talent**-løsningen installert, skal Attract- og Onboard-data være lagret i dette miljøet. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> **HCM Talent**-løsningen brukes også i Dynamics 365 Human Resources.
