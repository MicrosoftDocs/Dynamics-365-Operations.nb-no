---
title: Hva er nytt eller endret i Dynamics 365 Talent (6. mai 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a4571abdb0e104af0a0657c75bf5a6b5764345a
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023867"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (6. mai 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Velg valgfrie dokumenter ved tilbudsoppretting

Når du velger en tilbudspakkemal, blir du nå bedt om å velge de aktuelle, valgfrie dokumentene fra denne pakkemalen. Du kan legge til andre valgfrie dokumenter mens du klargjør tilbudet.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2282. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>Platform update 26 for Finance and Operations

Hvis du vil ha mer informasjon om Platform update 26 for Finance and Operations, kan du se [Forhåndsvisningsfunksjoner i Dynamics 365 Finance and Operations Platform Update 26 (mai 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-enhetsstøtte for egendefinerte felt

I denne ukens versjon støtter nå følgende enheter egendefinerte felt: Beregningsfrekvens for fordeler, Beregningssats for fordeler, Fordelstype, Arbeidskalender, Arbeidskalenderferie, Lønnssyklus og Arbeideridentifikasjonstyper.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Avslutning av masseregistrering og endring av nivågrunnlaget til Ansiennitetsdato oppdaterer ikke den første avsetningssatsen (318526)

Når du masseregistrerer ansatte og endrer nivågrunnlaget, gjenspeiler nå den første avsetningen nivågrunnlaget du valgte.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Arbeidsflyt som viser dupliserte plassholdere (313636)

Endringer i denne versjonen fjerner dupliserte plassholdere når arbeidsflytvarslinger sendes.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensjonsfelt blir ikke oppdatert når du bruker Åpne i Excel (176261)

Med denne versjonen kan du nå oppdatere finansdimensjonen ved hjelp av **Åpne i Excel** fra **Arbeider**-siden. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Arbeideradresse opprettet i Common Data Service synkroniseres ikke med Talent (317555)

Med denne endringen blir adresser som er opprettet i Common Data Service, oppdatert i Talent: Core HR.


## <a name="in-preview"></a>I forhåndsvisning

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ny side for å validere stillingshierarkidata

Personale (HR) og administratorer kan nå validere lederhierarkiet for eventuelle sirkelreferanser som kan ha blitt importert ved en feiltakelse. Du kan få tilgang til den nye siden fra **Organisasjonsstyring > Koblinger > Stillinger > Validering av stillingshierarki**.

### <a name="specify-reason-codes-on-leave-types"></a>Angi årsakskoder for permisjonstyper

Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og la de ansatte velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær

Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kravet kan finnes på grunn av firmapolicy eller forskriftsmessige krav. Du kan nå angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte angir en årsakskode for fraværstypen i forespørsler om fravær.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Angi en transaksjonsliste for permisjon og fravær for HR

Muligheten for å spore ansattes fravær og forstå hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte. HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at HR-ansatte kan vise årsakene bak saldoer.

## <a name="coming-soon"></a>Kommer snart

### <a name="indicate-instance-type-when-provisioning-talent"></a>Angi forekomsttype ved klargjøring av Talent

Når du klargjør en ny forekomst av Talent, vil du kunne angi om forekomsttypen er **Produksjon** eller **Sandkasse**, slik at du kan teste nye funksjoner tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til produksjonsforekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen sandkasse, kan du kontakte kundestøtte for å starte endringsforespørselen.
