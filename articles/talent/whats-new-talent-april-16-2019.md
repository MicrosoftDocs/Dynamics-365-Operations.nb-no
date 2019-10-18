---
title: Hva er nytt eller endret i Dynamics 365 Talent (16. april 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0781a479ebf37334d8eba18ea6d69d7cfb9db9ea
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024143"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (16. april 2019)?

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="process-auditing"></a>Prosessovervåking

Du kan nå spore endringer som gjøres i kandidater, ledige stillinger og stillingssøknader. Hvis du vil ha mer informasjon, kan du se [Spore endringer i rekrutteringsdata](process-auditing.md).

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2239. Tall i parentes refererer til støttenumre i Lifecycle Services (LCS).

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Enhetene Kompensasjonsområde, Kompensasjonsnivå, Fordelsalternativ og Kompetansetype i Common Data Service er oppdatert for å inkludere støtte for kundefelt

I denne versjonen har disse Common Data Service-enhetene blitt oppdatert slik at de inkluderer muligheten for å inkludere egendefinert felt som legges til via Talent: (Core HR).

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a>Støtte for ny Common Data Service-enhet: Kompensasjon, overdragelsesregler, Variabel plan for kompensasjon, Variabel kompensasjon

I denne versjonen er enhetene Kompensasjon, overdragelsesregler, Variabel plan for kompensasjon og Variabel kompensasjon lagt til Common Data Service. Disse enhetene støtter også egendefinerte felt som legges til via Talent: (Core HR).

### <a name="powerbi-refresh-issues-314342"></a>PowerBI-oppdateringsproblemer (314342)

Denne endringen løser et problem med PowerBI-rapporter slik at de oppdateres riktig.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>Kan ikke klikke direkte gjennom på overgangsoppgaver i ansattselvbetjening (303309)

Denne endringen gjør at brukere med ansattrollen kan velge og oppdatere overgangsoppgaver fra gjøremålslisten i Talent.

### <a name="performance-feedback-email-message-updated-309615"></a>E-postmelding med tilbakemelding om resultat er oppdatert (309615)

Med denne endringen vises en bekreftelsesmelding når tilbakemeldingen er sendt inn.

### <a name="missing-tables-in-word-template-308048"></a>Manglende tabeller i Word-mal (308048)

Med denne endringen vil bare kompetansen for den valgte medarbeideren vises i Word-dokumentet når du oppretter en Word-mal med ansatt- og kompetanseinformasjon.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>Når du bruker en sjekkliste for jobbavslutning, vises en feil. (299877)

Denne endringen løser et problem når det brukes en sjekkliste for jobbavslutning direkte fra arbeiderskjemaet.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tillate angivelse av årsakskoder for permisjonstyper

Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og gi de ansatte mulighet til å velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær

Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kan være på grunn av firmapolicy eller lovbestemte krav. Du kan nå angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte må angi en årsakskode for fraværstypen i forespørsler om fravær.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Angi transaksjonsliste for permisjon og fravær for HR

Sporing av ansattes fravær og forståelse av hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte. HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at det er mulig å vise årsakene bak saldoer.

## <a name="coming-soon"></a>Kommer snart

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Forbedringer av brukergrensesnittet for kontroll av dupliserte ansatte

Med denne endringen oppdages duplikater når du angir navnefelt, og statusen viser hvor mange duplikater som ble funnet. Du kan velge den angitte lenken for å åpne en ny side for å vurdere om du vil bruke resultatet som ble funnet. For å unngå å forstyrre dataregistreringen åpnes duplikatskjemaet ikke automatisk.

### <a name="email-support-for-alerts"></a>E-poststøtte for varsler

Med platform update 25 for Finance and Operations kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når de utløses av en hendelse.


