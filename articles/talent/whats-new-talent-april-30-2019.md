---
title: Hva er nytt eller endret i Dynamics 365 for Talent (30. april 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 112146ac46193e37b33bf429dc5a359f8cfaca94
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505381"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-30-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (30. april 2019)?

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringene som er beskrevet i denne delen, gjelder build nummer 8.1.2270. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Gi tilbakemelding

Alternativet for å gi tilbakemelding finner du på **Hjelp**-menyen (**?**) i Talent. Denne menyen gir tilgang til følgende ressurser:

- Tilbakemelding
- Hjelp
- Komme i gang
- Støtte
- Ideer
- Om

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Forbedringer av brukergrensesnittet for registrering av dupliserte ansatte

På grunn av denne endringen blir duplikater nå oppdaget når du angir navnefelt, og en statusindikator viser antall duplikater som er funnet. En angitt kobling åpner en side der du kan vurdere om du skal bruke et av duplikatene. For å unngå å forstyrre dataregistreringen åpnes ikke duplikatsiden automatisk. Du må velge koblingen for å åpne siden.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-enhetsstøtte for egendefinerte felt

I denne ukens versjon støtter nå følgende enheter egendefinerte felt: Ansettelse, Fordelstype og Lønnssyklus.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Det oppstår en feil når en jobbavslutningssjekkliste tilordnes (299877)

Denne endringen retter opp en feilmelding som vises når du tilordner en jobbavslutningssjekkliste til en ansatt utenfor avslutningsprosessen.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Koblingen for arbeidere som har sluttet, åpner feil arbeider (309939)

Denne endringen løser et problem som oppstår når du ansetter på nytt en ansatt fra en annen juridisk enhet og prøver å gå til den ansatte fra listen over arbeidere som har sluttet.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Kompensasjonskortet for ansattselvbetjening viser ikke sammendragsverdier når avansert sikkerhet er aktivert (315231)

Denne endringen løser et problem som oppstår når du bruker avansert kompensasjonssikkerhet. Når avansert sikkerhet er aktivert, viser ansattselvbetjening nå sammendragskompensasjonsbeløpene for både ansatte og ledere. Før endringen ble sammendragsverdier vist som 0 (null).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Hvis en stilling uten tittel opprettes i Common Data Service, blir det ikke opprettet en stilling i Talent (314562)

Denne ukens endringer løser et problem som oppstår når du oppretter stillinger i Common Data Service, men ikke angir en tittel.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Feilmelding i ytelsesjournalposter i ansattselvbetjening (314134)

Denne endringen retter opp et problem som oppstår når du knytter ytelsesmål til ytelsesjournalposter i ansattselvbetjening.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tillate angivelse av årsakskoder for permisjonstyper

Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og la de ansatte velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær

Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kravet kan finnes på grunn av firmapolicy eller forskriftsmessige krav. Du kan nå angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte angir en årsakskode for fraværstypen i forespørsler om fravær.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Angi en transaksjonsliste for permisjon og fravær for HR

Muligheten for å spore ansattes fravær og forstå hvordan fravær beregnes, hjelper ikke bare Personale (HR) med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte. HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at HR-ansatte kan vise årsakene bak saldoer.

## <a name="coming-soon"></a>Kommer snart

### <a name="email-support-for-alerts"></a>E-poststøtte for varsler

I platform update 26 kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når varslinger utløses av en hendelse.
