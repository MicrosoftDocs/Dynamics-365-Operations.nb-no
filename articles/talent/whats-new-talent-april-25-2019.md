---
title: Hva er nytt eller endret i Dynamics 365 Talent (23. april 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 53faf972759c8f770017fcd3a87920410988e626
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527195"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (23. april 2019)?

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2253. Tall i parentes refererer til støttenumre i Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-enhetsstøtte for egendefinerte felt
Med denne ukens versjon støtter følgende enheter egendefinerte felt: Kompensasjonsnivå, Fordelsalternativ, Kompetansetype og Kompensasjonsområde.

### <a name="additional-odata-entities-302992"></a>Ekstra OData-enheter (302992)
Følgende enheter støttes nå i OData: Yrkeserfaring for arbeider og Utdanning for arbeider.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Ytelsesjournalvedlegg for ledere og ansatte (308248)
Med denne versjonen er vedlegg nå tilgjengelige for både ledere og ansatte når de oppretter og oppdaterer ytelsesjournalposter.

### <a name="employee-rehire-flag-always-available-310047"></a>Flagg for ny ansettelse av ansatte er alltid tilgjengelig (310047)
Alternativet for å ansette ansatte på nytt er nå tilgjengelig for oppdatering utenfor avslutningsprosessen. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>Kan ikke endre navnet på **Min betalingsmåte** (308815)
Tilpassing er aktivert slik at etiketten **Min betalingsmåte** kan endres i ansattselvbetjening.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Finansdimensjoner mot en stilling kan ikke slettes (293908)
Finansdimensjoner kan nå fjernes når du ber om en endring i en eksisterende stilling og finansdimensjonene krysser firmagrenser. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Kunde kan ikke publisere data til Talent når data åpnes fra Excel (302955)
Denne endringen korrigerer et publiseringsproblem ved bruk av relaterte tabeller.

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
## <a name="known-issues"></a>Kjente problemer

### <a name="email-support-for-alerts"></a>E-poststøtte for varsler
Med Platform update 26 for Finance and Operations kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når de utløses av en hendelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]