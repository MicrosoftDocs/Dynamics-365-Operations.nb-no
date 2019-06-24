---
title: Hva er nytt eller endret i Dynamics 365 for Talent (13. mai 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591508"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (13. mai 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Talent.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-on-home-page"></a>Jobbgodkjenninger på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene under **Tilordnet til deg**, som viser jobb-ID, tittel, andre godkjennere og tilordnet dato. Brukere som sender en jobb for godkjenning, kan se gjennom jobbene under **Forespurt av deg**, som viser godkjennerne som fortsatt må godkjenne den sendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2297. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Angi forekomsttype ved klargjøring av Talent

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er **Produksjon** eller **Sandkasse**, slik at du kan teste nye funksjoner tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til **Produksjon**-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen **Sandkasse**, kan du kontakte [kundestøtten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) for å starte endringsforespørselen.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-enhetsstøtte for egendefinerte felt

I denne ukens versjon støtter nå følgende Common Data Service-enheter egendefinerte felt: Ansettelse, Beregningsfrekvens for fordeler, Beregningssats for fordeler, Arbeidskalenderferie og Identifikasjonstype.

### <a name="common-data-service-integration-page"></a>Common Data Service-integrasjonsside

Denne versjonen gir et nytt alternativ i **Systemadministrasjon > Koblinger > Integreringer > Common Data Service-konfigurasjon**. Med alternativet **Common Data Service-konfigurasjon** får en administrator eller databehandlingsadministrator litt fleksibilitet og innsikt i Common Data Service. Med dette alternativet kan du aktivere eller deaktivere Common Data Service-integrering med en Talent-forekomst og vise synkroniseringsdetaljer mellom Talent-forekomsten og Common Data Service.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Importere ytelsesdata med endelig ansattvurdering (316710)

I denne versjonen kan du importere historiske data for ansattvurdering. Feltet **FinalEmployeeRatingId** har nå skrivetillatelse.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Kan ikke opprette arbeideradresse i Common Data Service og synkronisere den med Talent (317555)

Denne endringen tillater synkronisering av adressedata som er opprettet i Common Data Service, med Talent.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side for å validere stillingshierarkidata

Personale (HR) og administratorer kan validere lederhierarkiet for eventuelle sirkelreferanser som kan ha blitt importert ved en feiltakelse. Du kan få tilgang til den nye siden fra **Organisasjonsstyring > Koblinger > Stillinger > Validering av stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angi årsakskoder for permisjonstyper

Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og la de ansatte velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær

Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kravet kan finnes på grunn av firmapolicy eller forskriftsmessige krav. Du kan angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte angir en årsakskode for fraværstypen i forespørsler om fravær.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Angi en transaksjonsliste for permisjon og fravær for HR

Muligheten for å spore ansattes fravær og forstå hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte. HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at HR-ansatte kan vise årsakene bak fridagssaldoer.
