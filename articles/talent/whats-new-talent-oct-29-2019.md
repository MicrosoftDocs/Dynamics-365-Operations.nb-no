---
title: Hva er nytt eller endret i Dynamics 365 Talent (29. oktober 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773883"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (29. oktober 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2586. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Slett parter uten roller skal være aktivert som standard (371233)

Når du klargjør et nytt miljø i Talent, er **Slett parter uten roller** aktivert som standard. Når du sletter en arbeider, blir ikke parten som er tilknyttet arbeideren, fjernet med mindre denne innstillingen er aktivert. Denne endringen begrenser like poster i den globale adresseboken når du har behov for å importere, endre eller importere arbeidere på nytt.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Utkast og annullerte permisjonsforespørsler må kunne slettes i Common Data Service (376999)

Med denne endringen kan du nå slette permisjonsforespørsler med statusen **utkast** eller **avbrutt** i Common Data Service.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Flere listeverdier i egendefinerte felt gjenspeiles ikke i Common Data Service når du klikker Bruk på egendefinerte felt-skjemaet (379599)

Når du legger til nye listeverdier i et eksisterende egendefinert felt som allerede er synkronisert med Common Data Service, er de nå tilgjengelige i Common Data Service etter at du har brukt endringer i **Egendefinerte felt**-skjemaet.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Bruk sjekklister for jobbintroduksjon på tvers av juridiske enheter når det finnes mer enn én ansettelse (371270)

I denne ukens frigivelse kan du bruke sjekklister på ansatte med mer enn ett ansettelsesforhold i **Arbeider-skjema > Sjekklister**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Åpen registrering for fordeler fra offentlig forhåndsvisning er fjernet

I forbindelse med vår kunngjøring i blogginnlegget [Strategiske investeringene i Core HR gir til store driftsfordeler](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) har Microsoft fjernet funksjonen for åpen registrering av fordeler fra den offentlige forhåndsvisningen. Ny funksjonalitet vil bli utgitt i fremtiden. Produksjonsbruk av funksjonen for åpen registrering for fordeler støttes ikke.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.

### <a name="feature-management-workspace"></a>Arbeidsområde for funksjonsbehandling

Funksjoner legges til og oppdateres i hver versjon. Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem.

Hvis du vil ha mer informasjon om endringene som kommer med funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
