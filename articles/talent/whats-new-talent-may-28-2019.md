---
title: Hva er nytt eller endret i Dynamics 365 Talent (28. mai 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 29e941ddab1b2746ccd74d6e335fec7742d1391e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529614"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-28-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (28. mai 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-on-home-page"></a>Jobbgodkjenninger på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene under **Tilordnet til deg**, som viser jobb-ID, tittel, andre godkjennere og tilordnet dato. Brukere som sender en jobb for godkjenning, kan se gjennom jobbene under **Forespurt av deg**, som viser godkjennerne som fortsatt må godkjenne den sendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2319.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-enhetsstøtte for egendefinerte felt

I denne versjonen støtter nå følgende Common Data Service-enheter egendefinerte felt: detaljer om beregningssats for fordeler, arbeidskalenderferielinje og ansettelse.

### <a name="copy-position-now-includes-payroll-details"></a>Kopier stilling inneholder nå lønnsdetaljer
Når du bruker **Kopier stilling** og velger alle alternativene, blir informasjon om lønnsdetaljer nå tatt med i kopieringsinformasjonen. 

## <a name="in-preview-in-core-hr"></a>I forhåndsvisning i Core HR

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begrens permisjonstypene i fritidforespørsler

Organisasjoner kan tilby mange forskjellige typer permisjon til ansatte. Noen av disse permisjonstypene er kanskje ikke riktige når ansatte skal kunne sende inn fritid, og administreres av personale (HR) i stedet. Ved hjelp av denne versjonen kan du konfigurere hvilke permisjonstyper ansatte kan sende inn fritidsforespørsler for. 

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side for å validere stillingshierarkidata

HR og administratorer kan validere lederhierarkiet for eventuelle sirkelreferanser som kan ha blitt importert ved en feiltakelse. Du kan få tilgang til den nye siden fra **Organisasjonsstyring > Koblinger > Stillinger > Validering av stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angi årsakskoder for permisjonstyper

Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og la de ansatte velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær

Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kravet kan finnes på grunn av firmapolicy eller forskriftsmessige krav. Du kan angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte angir en årsakskode for fraværstypen i forespørsler om fravær.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Angi en transaksjonsliste for permisjon og fravær for HR

Muligheten for å spore ansattes fravær og forstå hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte. HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at HR-ansatte kan vise årsakene bak fridagssaldoer.
